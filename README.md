# CompHound &ndash; Component Tracker

This is the CompHound project main landing page.

CompHound is a cloud-based universal component and asset usage analysis, reporting, bill of materials, visualisation and navigation project providing sample code for two presentations on connecting the desktop with the cloud
at [RTC Europe](http://www.rtcevents.com/rtc2015eu) in Budapest end of October
and [Autodesk University](http://au.autodesk.com) in Las Vegas in December.

It currently consists of two parts:

- [CompHoundWeb](https://github.com/CompHound/CompHoundWeb),
a Node.js web server, mongo database and
[Autodesk View and Data API](https://developer.autodesk.com) viewer.
- [CompHoundRvt](https://github.com/CompHound/CompHoundRvt),
a Revit add-in to populate the CompHound web database with ±BIM family instances.

This project is based on and derived from the node.js mongodb web server for the **FireRating in the Cloud** sample, consisting of the
[FireRatingCloud](https://github.com/jeremytammik/FireRatingCloud) C# .NET REST API client Revit add-in and the
[fireratingdb](https://github.com/jeremytammik/firerating) Node.js mongoDB web server.

In addition to that, this project also sports a user interface, including report, bill of material,
[Autodesk View and Data API](https://developer.autodesk.com) 2D and 3D model analysis, viewing and navigation functionality.

You can [try it out live](#try-it-out-live) and
read the [detailed articles](#further-reading) describing
the entire project implementation and evolution below.


## Try it out Live

You can explore this app up and running live.

Here is the mongolab-hosted database that we are using:
[mongolab.com/databases/comphound](https://mongolab.com/databases/comphound).

It contains the collection of
[component instances](https://mongolab.com/databases/comphound/collections/instances).
The only occurrences that I exported so far are from the standard Revit sample file `rst_advanced_sample_project.rvt`.
You can add more yourself by running the
[CompHoundRvt](https://github.com/CompHound/CompHoundRvt) add-in in any other Revit BIM of your choice.

The node.js web server driving the database via mongoose is hosted on
[Heroku](https://dashboard.heroku.com), and its URL is
[https://comphound.herokuapp.com](https://comphound.herokuapp.com).

Its REST API is accessible via the route [/api/v1](https://comphound.herokuapp.com/api/v1).

[/api/v1/instances](https://comphound.herokuapp.com/api/v1/instances) should in theory return all database entries, but it will fail with an application error due to too large data.

From version 0.0.25 onwards, the REST API
route [/api/v1/auth](https://comphound.herokuapp.com/api/v1/auth) provides
access to the [View and Data API](https://developer.autodesk.com) authorisation token.

However, you can use [/api/v1/instances/:id](https://comphound.herokuapp.com/api/v1/instances/48891eaa-9041-405b-a10f-f06585de3cbb-0001de6d) to retrieve the JSON document for a single specific entry.

Finally, it sports the beginnings of a user interface that currently provides the following access points:

- [/](https://comphound.herokuapp.com) &ndash; say hello.
- [/hello/:message](https://comphound.herokuapp.com/hello/jeremy) &ndash; reply with the message passed in.
- [/html/count](https://comphound.herokuapp.com/html/count) &ndash; return the number of database entries.
- [/www/instances1](https://comphound.herokuapp.com/www/instances1) &ndash;  list all the database entries in a table &ndash; this can take a long time.
- [/datatable2](https://comphound.herokuapp.com/datatable2) &ndash; display a datatable navigation interface through the instance records.

In the long run, most of these access points can be shut down again.

Instead, one single main `index` entry point will display the datatable listing the component occurrences as well as provide access to the still missing reporting, viewing and model navigation functionality.


## Further Reading

The following discussions
by [The 3D Web Coder](http://the3dwebcoder.typepad.com)
and [The Building Coder](http://thebuildingcoder.typepad.com)
describe the entire project implementation and evolution:

- [Project definition and christening](http://the3dwebcoder.typepad.com/blog/2015/09/comphound-jsfiddle-and-my-first-react-component.html).
- [First implementation](http://the3dwebcoder.typepad.com/blog/2015/09/comphound-restsharp-mongoose-put-and-post.html#2) based on
[fireratingdb](https://github.com/jeremytammik/firerating) and
[FireRatingCloud](https://github.com/jeremytammik/FireRatingCloud).
- [Steps towards a database table view](http://the3dwebcoder.typepad.com/blog/2015/09/towards-a-comphound-mongo-database-table-view.html).
- [The CompHound Mongoose DataTable](http://the3dwebcoder.typepad.com/blog/2015/09/the-comphound-mongoose-datatable.html)
- [CompHound Heroku Deployment](http://the3dwebcoder.typepad.com/blog/2015/09/comphound-heroku-deployment-and-urban-farming.html)


## Author

Jeremy Tammik,
[The Building Coder](http://thebuildingcoder.typepad.com) and
[The 3D Web Coder](http://the3dwebcoder.typepad.com),
[ADN](http://www.autodesk.com/adn)
[Open](http://www.autodesk.com/adnopen),
[Autodesk Inc.](http://www.autodesk.com)


## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT).
Please see the [LICENSE](LICENSE) file for full details.
