rapidsms-threadless-router
==========================

A `RapidSMS <https://github.com/rapidsms/rapidsms>`_ router implementation that
removes the threading functionality from the legacy Router class.  Rather, all
inbound requests are handled via the main HTTP thread.  Backends can optionally
pass requests to a message queue for out-of-band responses.
``threadless_router`` attempts to:

* Make RapidSMS backends more Django-like.  Use Django's URL routing and views to handle inbound HTTP requests.
* Remove clutter and complexity of route process and threaded backends.
* Ease testing -- no more ``threading`` or ``Queue`` modules slowing down tests.

Please refer to the `documentation <http://rapidsms-threadless-router.readthedocs.org/>`_ for more details.

Development by `Caktus Consulting Group <http://www.caktusgroup.com/>`_.
