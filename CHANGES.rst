Release 0.10 (dev)
------------------

*Nothing yet.*


Release 0.9 (Apr. 4, 2014)
--------------------------

- Add ``VideoBackend.template_name`` and rendering embed code from file.

- Allow relative sizes in template tag
  (`#19 <https://github.com/yetty/django-embed-video/pull/19>`_).

- Fix handling invalid urls of SoundCloud.
  (`#21 <https://github.com/yetty/django-embed-video/issues/21>`_).

- Catch ``VideoDoesntExistException`` and ``UnknownBackendException`` in
  template tags and admin widget.

- Add base exception ``EmbedVideoException``.


Release 0.8 (Feb. 22, 2014)
---------------------------

- Add ``EMBED_VIDEO_TIMEOUT`` to settings.

- Fix renderering template tag if no url is provided
  (`#18 <https://github.com/yetty/django-embed-video/issues/18>`_)

- If ``EMBED_VIDEO_TIMEOUT`` timeout is reached in templates, no exception is
  raised, error is just logged.

- Fix default size in template tag.
  (`See more... <https://github.com/yetty/django-embed-video/commit/6cd3567197d6fdc31bc63fb799815e8368128b90>`_)


Release 0.7 (Dec. 21, 2013)
---------------------------

- Support for sites running on HTTPS

- ``embed`` filter is deprecated and replaced by ``video`` filter.

- caching for whole backends was removed and replaced by caching properties

- minor improvements on example project (fixtures, urls)


Release 0.6 (Oct. 04, 2013)
---------------------------

- Ability to overwrite embed code of backend

- Caching backends properties

- PyPy compatibility

- Admin video mixin and video widget


Release 0.5 (Sep. 03, 2013)
---------------------------

- Added Vimeo thumbnails support

- Added caching of results

- Added example project

- Fixed template tag embed

- Fixed raising UnknownIdException in YouTube detecting.



Release 0.4 (Aug. 22, 2013)
---------------------------

- Documentation was rewrited and moved to http://django-embed-video.rtfd.org/ .

- Custom backends
  (http://django-embed-video.rtfd.org/en/latest/examples.html#custom-backends).

- Improved YouTube and Vimeo regex.

- Support for Python 3.

- Renamed ``base`` to ``backends``.



Release 0.3 (Aug. 20, 2013)
---------------------------

- Security fix: faked urls are treated as invalid. See `this page
  <https://github.com/yetty/django-embed-video/commit/d0d357b767e324a7cc21b5035357fdfbc7c8ce8e>`_
  for more details.

- Fixes:

  - allow of empty video field.

  - requirements in setup.py

- Added simplier way to embed video in one-line template tag::

    {{ 'http://www.youtube.com/watch?v=guXyvo2FfLs'|embed:'large' }}

- ``backend`` variable in ``video`` template tag.

  Usage::

    {% video item.video as my_video %}
        Backend: {{ my_video.backend }}
    {% endvideo %}


Release 0.2 (June 25, 2013)
---------------------------

- Support of SoundCloud

Release 0.1 (June 1, 2013)
--------------------------

- Initial release
