Hey! Thanks for checking this out!
===

This is a T4 template that will generate POCO's (Plain Old CLR Objects) from your database tables and columns.

Here is all you need to do:

1. Drop the 2 T4 templates into your Visual Studio Project.
2. Open up the "Pocos.tt" template
3. Set your own values for the namespaceName, serverName, and databaseName
4. Save the template and it should promt you to run!  Just hit OK and watch the magic happen!

After that, you can continue to run the T4 template as you update the database, or you can delete the templates and keep the POCO's.

Limitations:
---
1. Only works with Windows Authentication and configuration values are hardcoded into the template.  Ideally this could work off AppSettings (Web.config/app.config) and allow for SQL Server authentication as well.
2. Generates POCO's for all tables in the database (no automatic filtering).  Ideally a schema, prefix, or regex filter would be nice.
3. The only Data Annotation attribute that is currently added is the Key attribute.  Ideally we will support all related validation attributes.
