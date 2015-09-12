Currently, this project is in sketch-pad mode.

Imagine being able to whip up a small web application by describing some business entities, setting their parameters (fields) and relations, seeing the automatically generated XML, then popping up an XSLT editor to apply the layout.

Here are some ideas:
  * The interface for this application is implemented using XUL as a firefox plugin
  * The backend application is created using object oriented PHP. PHP scripts/classes extend and utilise [XAO](http://xao-php.sf.net).
  * Forms can be semi-automatically generated to populate the created business objects (XAO already supports a form fields API)
  * XAB can ship with canned templates to handle default display of forms and (error) message reporting.
  * Looking at using PHP5s default shipped SQLite which means the system does not require an RDBMS server. It may be possible for the user to choose which database system they would like to use based on the XAO db drivers (contains it own  object oriented RDBMS abstraction layer). XAO also has a general "entities" API which is designed to sit atop said abstraction layer.
  * XAB might use ajax requests to have a PHP (server) based utility do all the "dirty work" - including create on database tables/views and PHP class script files on the server.
  * template libraries are resident with the XUL application as are the "user templates" (My Templates). Anyone want to design/contribute a XUL based XSLT editor???
  * need to think of a clever way to just drop in pre-built application modules (OO packages). I want a central registry of modules which is accessed by a module browser built into the XAB wizard. It needs to be transparent to the build process (not sending the user off on a wild goose chase looking for zip files etc.).
  * modules will have a manifest which allows them to embed PHP scripts, XSLT template (modules), and other files (images, javascript, css).
  * XAO will automatically detect which version of XSL is in use and then invoke the appropriate processor. There will also be an option to allow client-side XSL transformation.

For updates and more info, check out the weblog.