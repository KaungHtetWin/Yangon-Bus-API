# Yangon-Bus-API

### Note
All Data are provided by [Yangon Bus website](http://yangonbus.com/) under the terms of the YRTA Open Data Licence version 1.0 [Yangon Bus website](http://data.yangonbus.com/license.html).

Update data are avaliable (Bus no 62-81).Creating with special tool.This tool will be open soruce soon.

This API is only for development pourpose.It's not ready for production.

### API End Points
 >* All buses https://ygnbus.herokuapp.com/api/bus/
 >* Each Bus https://ygnbus.herokuapp.com/api/bus/1 
 >* All Bus stops https://ygnbus.herokuapp.com/api/busstop 
 >* Routing https://ygnbus.herokuapp.com/api/route/287/523
 
 
### Get API Key
>* Login With GitHub https://ygnbus.herokuapp.com/login
>*  Add API key in Authorization header of request.

### Here is complete json format for bus,bus route and bus stop
	{
    "bus":{
     "busID":1,
     "busName":"၁",
     "busTypeID":{
      "busTypeName":"အပြာ",
      "busColor":"#405caa",
      "busDescription":"မြောက်ပိုင်းခရိုင်အခြေပြု လိုင်းများ"
     }
    },
    "busRoute":{
     "name":"လှည်းကူးဈေးရှေ့↔စံပြဈေး",
     "route":{
      "coordinates":[[lng,lat],[lng,lat]],
      "type":"LineString"
    },
    "busStops":[
     {
      "busStopID":101,
      "busStopName":"ကားကြီးဂိတ်",
      "busStopPoint":{
       "type":"Point",
       "coordinates":[lng,lat]
      }
     },
     {
      "busStopID":85,
      "busStopName":"ကျိုက္ကစံဘုရား",
      "busStopPoint":{
       "type":"Point",
       "coordinates":[lng,lat]
      }
     }
    ]
    }
    
### Routing
>* https://ygnbus.herokuapp.com/api/route/287/523
>* 287 start bustop id and 523 is end bustop id.
>* support multiple result.
>* "path" is routing result and "cost" is approximate distance(km) between start busstop and end busstop.
>* In "path" all number stand for bustop id and "B" is bus id (eg., B41 is bus no 41).

### Routing Result 

	[
	  {
	    "path": [
	      "287",
	      "B41",
	      "292",
	      "B20",
	      "454",
	      "B9",
	      "523"
	    ],
	    "cost": 11.385357244665474
	  },
	  {
	    "path": [
	      "287",
	      "B21",
	      "1375",
	      "B17",
	      "819",
	      "B32",
	      "523"
	    ],
	    "cost": 34.50324318404451
	  },
	  {
	    "path": [
	      "287",
	      "B39",
	      "1513",
	      "B42",
	      "545",
	      "B33",
	      "523"
	    ],
	    "cost": 35.169001135060846
	  }
	]
