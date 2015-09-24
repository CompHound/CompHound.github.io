# CompHound.github.io

CompHound project landing page.

CompHound is a cloud-based universal component and asset usage analysis, report, bill of material and visualisation project providing sample code for two presentations on connecting the desktop with the cloud at
[RTC Europe](http://www.rtcevents.com/rtc2015eu) in Budapest end of October and
[Autodesk University](http://au.autodesk.com) in Las Vegas in December.

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

For more information, please refer to
[The 3D Web Coder](http://the3dwebcoder.typepad.com),
[The Building Coder](http://thebuildingcoder.typepad.com) and
the detailed articles describing the entire project implementation and evolution:

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
