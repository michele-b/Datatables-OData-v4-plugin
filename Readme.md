#Datatables-OData-v4-plugin
Enables jQuery DataTables to read and display data from an OData service.
It support server-side operations like:
* Pagination
* Sorting
* Global and column filtering
* Numeric, date and string types
* Range filter for numeric and date types
* V4 OData support (only)
* JSONP requests

## How to use

```javascript
$('table#people').dataTable({
    "oDataUrl": "/odata/People",
  	"oDataViaJsonp": false,	// set to true for cross-domain requests
    "oDataAbort": false, // set to true to cancel previous on-going request
    "ajax": ajaxOData,
    "serverSide": true, // set to true for OData server side filtering and sorting 
    "columns": [
      { data: "Id", type: "num" },
      { data: "Name" },
      { data: "Surname" },
      { data: "BirthPlace" },
      { data: "BirthDate", type: "date" }
  	],
});
```

### Notes
* Type for numeric and date columns must be set in the right way
* JQuery Globalize is optionally used for number and date parsing

## Author
Michele Bersini, inspired from Vida Popovic OData connector (Thanks)

## Copyright and license
Copyright 2016 Michele Bersini under [the MIT license](https://opensource.org/licenses/MIT).
