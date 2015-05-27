HbbTV Application Toolkit
==============

**HAT** provides a CMS with a set of GUI templates that can be filled with content via an easy-to-use HTML5-based user interface. A REST-API to the content model of the HbbTV App Toolkit SE’s CMS allows its integration into the CMS used by content creators in their production environment. In addition to the CMS the **HbbTV App Toolkit SE** supports HbbTV developers by providing a library with solutions for recurrent tasks, e.g. navigation through a button list, scrollable elements, channel change, etc.


HbbTV Application Toolkit SE Specification
--------------
The **HbbTV Application Toolkit** includes a collection of templates, colour themes and modules:

- Broadcast
- Video
- Image
- Text
- Gallery
- Social Feed
- Popup
- Menu
- Layout

The editor can choose between various templates and color themes. These templates must be filled with media modules. Modules also can have pop-ups. By creating more then one template a menu will be built. A valid generated JSON for a HbbTV app could have the following structure:


Generated JSON
--------------
```
{
   "_id":"1234567890",
   "data":{
      "app":{
         "title":"App Title",
         "logoUrl":"http://www.logo.url",
         "backgroundImage":"/assets/bgr.png",
         "colorPattern":"mauer",
         "secondScreen":"true"
      },
      "pages":{
         "landingPage":{
            "layout":"template_1",
            "title":"LandingPage Title",
            "shorttitle":"LandingPage Shorttile",
            "content":{
               "t1_container1":{
                  "type":"broadcast",
                  "navigable":"false"
               },
               "t1_container2":{
                  "type":"scribble",
                  "title":"Live-Blog",
                  "id":"1234567890",
                  "navigable":"true"
               }
            }
         }
      }
   },
   "title":"",
   "__v":0,
   "alterationDate":"2014-10-29T06:48:28.814Z",
   "creationDate":"2014-10-27T02:00:58.543Z"
}
```

getHbbTVApp
--------------

Method                  | GET
-------------           | -------------
Call                    | http://[server]/api/apps/{indexid}
Path Parameter          | **indexid**: Index to be used
Query Parameter         | None
Headers                 | -
Body                    | SearchRequestType encoded as JSON String
Response                | HTTP 200 with body of AssetStatusResponseType
Sample Request          | http://hat.fokus.fraunhofer.de:8080/api/apps/5407e03d36d96e7456771d98

putHbbTVApp
--------------

Method                  | PUT
-------------           | -------------
Call                    | http://[server]/api/apps/{indexid}
Path Parameter          | **indexid**: Index to be used
Query Parameter         | None
Headers                 | -
Body                    | SearchRequestType encoded as JSON String
Response                | HTTP 200 with body of AssetStatusResponseType
Sample Request          | http://hat.fokus.fraunhofer.de:8080/api/apps/5407e03d36d96e7456771d98

deleteHbbTVApp
--------------
  
Method                  | DELETE
-------------           | -------------
Call                    | http://[server]/api/apps/{indexid}
Path Parameter          | **indexid**: Index to be used
Query Parameter         | None
Headers                 | -
Body                    | SearchRequestType encoded as JSON String
Response                | HTTP 200 with body of AssetStatusResponseType
Sample Request          | http://hat.fokus.fraunhofer.de:8080/api/apps/5407e03d36d96e7456771d98



Licence summary
--------------

Use of HbbTV application authoring tool: free-of-charge and "as is". Basic set of features: Provided free-of-charge without limitations. Additional selected premium features: Provided free-of-charge for non-commercial evaluation under FIWARE Customised extension: Agreement on case-by-case basis.

Licence type
--------------

Open source: No
Proprietary: No
Evaluation licence: Yes
Licence features

Commercial use: Yes
Modifications allowed: No
Distribution allowed: No
Include copyright: Required
Include original: Not applicable
State changes: Not applicable
Disclose source code: Not required
Licence fee

Free use of authoring environment to create HbbTV applications with specified subset of components. Additional selected premium features are provided free-of-charge for non-commercial use under the FIWARE programme. Further components might be released in the future and tailored extensions can be provided on a case-by-case basis.

Copyright statement
--------------

Copyright (c) 2013 Institut fuer Rundfunktechnik GmbH, Fraunhofer Institute for Open Communication Systems FOKUS

Full licence

http://hat.fokus.fraunhofer.de:8080/license/license.txt

**©Fraunhofer FOKUS**