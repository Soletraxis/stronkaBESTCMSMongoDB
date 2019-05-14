# BESTCms

App created with stapi and mongoDB.

notes:
1) http://help.strapi.io/customize/custom-populate-data-rest-api <- use to fix issue with not nesting data

`const populateOpt = [{
      path: "menus",
      populate: {
        path: "menus",
        populate: {
          path: "menus"
        }
      }
    }, {
      path: "menu",
      populate: {
        path: 'menu'
      }
    }]` is what fixed it.

2) For some reason I had to make many to many relation only to enable changing order in menu.
To make this work use:https://github.com/strapi/strapi/issues/2166
