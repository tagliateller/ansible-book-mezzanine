cd playbooks
vagrant up

== akt. Zustand - Fehler in Task. Wird django irgendwo installiert ?

TASK: [mezzanine | sync the database, apply migrations, collect static content] *** 
failed: [web] => (item=syncdb) => {"cmd": "python manage.py syncdb --noinput", "failed": true, "item": "syncdb", "path": "/home/vagrant/mezzanine-example/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games", "state": "absent", "syspath": ["/home/vagrant/.ansible/tmp/ansible-tmp-1455969463.65-35143423229871", "/usr/lib/python2.7", "/usr/lib/python2.7/plat-x86_64-linux-gnu", "/usr/lib/python2.7/lib-tk", "/usr/lib/python2.7/lib-old", "/usr/lib/python2.7/lib-dynload", "/usr/local/lib/python2.7/dist-packages", "/usr/lib/python2.7/dist-packages"]}
msg: 
:stderr: Traceback (most recent call last):
  File "manage.py", line 28, in <module>
    execute_from_command_line(sys.argv)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/__init__.py", line 399, in execute_from_command_line
    utility.execute()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/__init__.py", line 392, in execute
    self.fetch_command(subcommand).run_from_argv(self.argv)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 242, in run_from_argv
    self.execute(*args, **options.__dict__)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 284, in execute
    self.validate()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 310, in validate
    num_errors = get_validation_errors(s, app)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/validation.py", line 34, in get_validation_errors
    for (app_name, error) in get_app_errors().items():
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/db/models/loading.py", line 196, in get_app_errors
    self._populate()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/db/models/loading.py", line 78, in _populate
    self.load_app(app_name)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/db/models/loading.py", line 99, in load_app
    models = import_module('%s.models' % app_name)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/utils/importlib.py", line 40, in import_module
    __import__(name)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/compressor/models.py", line 1, in <module>
    from compressor.conf import CompressorConf  # noqa
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/compressor/conf.py", line 5, in <module>
    from django.template.utils import InvalidTemplateEngineError
ImportError: No module named utils

failed: [web] => (item=migrate) => {"cmd": "python manage.py migrate --noinput", "failed": true, "item": "migrate", "path": "/home/vagrant/mezzanine-example/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games", "state": "absent", "syspath": ["/home/vagrant/.ansible/tmp/ansible-tmp-1455969464.38-278155290376563", "/usr/lib/python2.7", "/usr/lib/python2.7/plat-x86_64-linux-gnu", "/usr/lib/python2.7/lib-tk", "/usr/lib/python2.7/lib-old", "/usr/lib/python2.7/lib-dynload", "/usr/local/lib/python2.7/dist-packages", "/usr/lib/python2.7/dist-packages"]}
msg: 
:stderr: Traceback (most recent call last):
  File "manage.py", line 28, in <module>
    execute_from_command_line(sys.argv)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/__init__.py", line 399, in execute_from_command_line
    utility.execute()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/__init__.py", line 392, in execute
    self.fetch_command(subcommand).run_from_argv(self.argv)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 242, in run_from_argv
    self.execute(*args, **options.__dict__)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 284, in execute
    self.validate()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 310, in validate
    num_errors = get_validation_errors(s, app)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/validation.py", line 34, in get_validation_errors
    for (app_name, error) in get_app_errors().items():
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/db/models/loading.py", line 196, in get_app_errors
    self._populate()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/db/models/loading.py", line 78, in _populate
    self.load_app(app_name)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/db/models/loading.py", line 99, in load_app
    models = import_module('%s.models' % app_name)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/utils/importlib.py", line 40, in import_module
    __import__(name)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/compressor/models.py", line 1, in <module>
    from compressor.conf import CompressorConf  # noqa
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/compressor/conf.py", line 5, in <module>
    from django.template.utils import InvalidTemplateEngineError
ImportError: No module named utils

failed: [web] => (item=collectstatic) => {"cmd": "python manage.py collectstatic --noinput", "failed": true, "item": "collectstatic", "path": "/home/vagrant/mezzanine-example/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games", "state": "absent", "syspath": ["/home/vagrant/.ansible/tmp/ansible-tmp-1455969464.99-271520629313900", "/usr/lib/python2.7", "/usr/lib/python2.7/plat-x86_64-linux-gnu", "/usr/lib/python2.7/lib-tk", "/usr/lib/python2.7/lib-old", "/usr/lib/python2.7/lib-dynload", "/usr/local/lib/python2.7/dist-packages", "/usr/lib/python2.7/dist-packages"]}
msg: stdout: Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/conf/static/mezzanine/css/admin/settings.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/robots.txt'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/fonts/glyphicons-halflings-regular.ttf'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/fonts/glyphicons-halflings-regular.svg'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/fonts/glyphicons-halflings-regular.eot'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/fonts/glyphicons-halflings-regular.woff'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/js/bootstrap-extras.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/js/bootstrap.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/js/respond.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/js/html5shiv.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/img/favicon.ico'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/chosen/chosen-sprite-dark.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/chosen/chosen-sprite.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/chosen/chosen.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/chosen/chosen-0.9.12.jquery.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/jquery.form.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/jquery-ui-1.9.1.custom.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/jquery.tools.toolbox.expose.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/tinymce_setup.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/jquery-1.7.1.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/editable.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/jquery.tools.overlay.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/admin/keywords_field.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/admin/ajax_csrf.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/admin/login.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/admin/collapse_backport.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/admin/navigation.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/js/admin/dynamic_inline.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/img/loadingAnimation.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/tinymce.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/editable.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/jquery-ui-1.9.1.custom.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/jquery-ui-1.9.1.custom.min.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_glass_75_e6e6e6_1x400.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_highlight-soft_75_cccccc_1x100.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_glass_65_ffffff_1x400.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-icons_222222_256x240.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_glass_75_dadada_1x400.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-icons_454545_256x240.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_flat_75_ffffff_40x100.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-icons_2e83ff_256x240.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_glass_95_fef1ec_1x400.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-icons_888888_256x240.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-icons_cd0a0a_256x240.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_glass_55_fbf9ee_1x400.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/smoothness/images/ui-bg_flat_0_aaaaaa_40x100.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/admin/global.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/admin/dashboard.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/mezzanine/css/admin/rtl.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/test/image.jpg'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/test/gallery.zip'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/css/mezzanine.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/css/bootstrap-theme.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/css/bootstrap.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/admin/img/admin/README'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/admin/img/admin/arrow-up.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/admin/img/admin/arrow-down.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/core/static/admin/img/admin/icon_deletelink.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/forms/static/mezzanine/js/admin/form_entries.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/forms/static/mezzanine/css/admin/form.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/forms/static/mezzanine/css/admin/form_entries.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/pages/static/mezzanine/js/admin/page_tree.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/pages/static/mezzanine/js/admin/jquery.mjs.nestedSortable.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/pages/static/mezzanine/css/admin/page_tree.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/galleries/static/mezzanine/js/magnific-popup.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/galleries/static/mezzanine/css/magnific-popup.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/mezzanine/galleries/static/mezzanine/css/admin/gallery.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/jquery.uploadify.v2.1.4.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/uploadify.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/jquery-1.4.2.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/uploadify.swf'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/cancel.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/uploadify.allglyphs.swf'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/swfobject.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/expressInstall.swf'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/uploadify/jquery.uploadify.v2.1.4.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/js/FB_TinyMCE4.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/js/FB_FileBrowseField.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/js/AddFileBrowser.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/js/TinyMCEAdmin.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/js/FB_TinyMCE.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/js/FB_CKEditor.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/js/filebrowser-popup.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_delete.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_rename.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_type_folder.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_type_.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_select_disabled.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_show.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_type_document.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_showversions_hover.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_type_image.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_type_audio.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_rename_hover.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_delete_hover.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_select.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_showversions.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_type_code.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_type_video.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_select_hover.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/img/filebrowser_icon_show_hover.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/css/filebrowser.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/filebrowser_safe/static/filebrowser/css/rtl.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/admin/js/actions.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/admin/js/actions.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/js/admin/Changelist.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/js/admin/Inline.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/js/admin/CollapsedInlineFieldsets.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icon_calendar.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icon_clock.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/grappelli-icon.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-th-ascending.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon_fieldset_collapse-closed.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_add-m2m_horizontal.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-no.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-calendarnav_next.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_add-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-unknown.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_remove-m2m_horizontal-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-related_lookup-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-actionlist_changelink-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_add-inactive.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-closehandler-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-calendarnav_previous.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon_inline-item-tools_closehandler.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-clock-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-actionlist_addlink.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-addhandler.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-yes.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-actions_changelist.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-fb_show-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-menulist_internal.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_add-m2m_vertical.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_remove-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon_inline-item-tools_openhandler.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-add_another-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-viewsitelink.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-th-descending.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon_fieldset_collapse-open.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-deletelink.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-addlink-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-related_lookup.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-closehandler.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-actionlist_deletelink.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon_inline-item-tools_addhandler.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-clock.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_remove-m2m_horizontal.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-actionlist_addlink-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_add.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-draghandler-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-changelink-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-addlink.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_manage.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-addhandler-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_remove.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-deletelink-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-fb_show.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-actionlist_changelink.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-openhandler-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-menulist_external.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-changelink.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_remove-m2m_vertical.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-calendar-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-openhandler.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-add_another.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-draghandler.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-inline_item_tools-viewsitelink-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_remove-inactive.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-menulist_internal-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_add-m2m_vertical-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_remove-m2m_vertical-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-menulist_external-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-calendar.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-bookmark_manage-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-selector_add-m2m_horizontal-hover.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/icons/icon-searchbox.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon-unknown.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/nav-bg-grabber.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/deleted-overlay.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tooltag-add.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_success.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/selector-remove.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/arrow-up.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon-yes.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tool-left_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/nav-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/inline-restore.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/inline-delete.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/selector-removeall.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/changelist-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/inline-splitter-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tool-right.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tooltag-arrowright_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon-no.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tooltag-add_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/selector-addall.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/selector_stacked-add.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/selector-add.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/changelist-bg_rtl.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/selector_stacked-remove.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/arrow-down.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/nav-bg-reverse.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/selector-search.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_deletelink.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_changelink.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_calendar.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/inline-delete-8bit.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/chooser_stacked-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_clock.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tool-left.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_addlink.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/chooser-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/inline-restore-8bit.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/default-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_alert.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_searchbox.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/default-bg-reverse.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/icon_error.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tooltag-arrowright.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/img/admin/tool-right_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/tables.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/forms.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/modules.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/dashboard.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/typography.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/login.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/rtl.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/widgets.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/reset.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/base.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/changelist.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/webkit-gradients.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/grappelli_safe/static/grappelli/css/documentation.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/inlines.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/jquery.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/urlify.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/inlines.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/collapse.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/core.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/jquery.init.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/SelectBox.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/collapse.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/timeparse.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/prepopulate.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/LICENSE-JQUERY.txt'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/SelectFilter2.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/jquery.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/calendar.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/prepopulate.min.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/admin/DateTimeShortcuts.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/js/admin/RelatedObjectLookups.js'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon-unknown.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/nav-bg-grabber.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/deleted-overlay.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tooltag-add.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_success.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon-yes.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tool-left_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/nav-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/inline-restore.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/inline-delete.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/changelist-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/inline-splitter-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tool-right.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tooltag-arrowright_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/selector-icons.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon-no.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tooltag-add_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/sorting-icons.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/changelist-bg_rtl.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/nav-bg-reverse.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/selector-search.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_deletelink.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_changelink.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_calendar.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/inline-delete-8bit.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/chooser_stacked-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_clock.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/nav-bg-selected.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tool-left.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_addlink.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/chooser-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/inline-restore-8bit.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/default-bg.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_alert.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_searchbox.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/default-bg-reverse.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/icon_error.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tooltag-arrowright.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/tool-right_over.gif'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/gis/move_vertex_off.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/img/gis/move_vertex_on.png'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/changelists.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/forms.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/dashboard.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/login.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/rtl.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/widgets.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/base.css'
Copying '/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/admin/static/admin/css/ie.css'

:stderr: Traceback (most recent call last):
  File "manage.py", line 28, in <module>
    execute_from_command_line(sys.argv)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/__init__.py", line 399, in execute_from_command_line
    utility.execute()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/__init__.py", line 392, in execute
    self.fetch_command(subcommand).run_from_argv(self.argv)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 242, in run_from_argv
    self.execute(*args, **options.__dict__)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 285, in execute
    output = self.handle(*args, **options)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/core/management/base.py", line 415, in handle
    return self.handle_noargs(**options)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/staticfiles/management/commands/collectstatic.py", line 173, in handle_noargs
    collected = self.collect()
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/staticfiles/management/commands/collectstatic.py", line 102, in collect
    for finder in finders.get_finders():
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/staticfiles/finders.py", line 253, in get_finders
    yield get_finder(finder_path)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/utils/functional.py", line 32, in wrapper
    result = func(*args)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/contrib/staticfiles/finders.py", line 261, in _get_finder
    Finder = import_by_path(import_path)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/utils/module_loading.py", line 26, in import_by_path
    sys.exc_info()[2])
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/utils/module_loading.py", line 21, in import_by_path
    module = import_module(module_path)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/django/utils/importlib.py", line 40, in import_module
    __import__(name)
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/compressor/finders.py", line 1, in <module>
    from compressor.utils import staticfiles
  File "/home/vagrant/mezzanine-example/local/lib/python2.7/site-packages/compressor/utils/staticfiles.py", line 3, in <module>
    from django.apps import apps
django.core.exceptions.ImproperlyConfigured: Error importing module compressor.finders: "No module named apps"


FATAL: all hosts have already failed -- aborting

PLAY RECAP ******************************************************************** 
           to retry, use: --limit @/home/robert/mezzanine-across-hosts.retry

db                         : ok=7    changed=6    unreachable=0    failed=0   
web                        : ok=6    changed=5    unreachable=0    failed=1   

Ansible failed to complete successfully. Any error output should be
visible above. Please fix these errors and try again.
robert@c3p0:~/workspace/ansible-book-mezzanine/classicvm/playbooks$ 
