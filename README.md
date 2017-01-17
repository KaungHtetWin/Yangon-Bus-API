# Yangon-Bus-API

### Note
All Data are provided by [Yangon Bus website](http://yangonbus.com/) under the terms of the YRTA Open Data Licence version 1.0 [Yangon Bus website](http://data.yangonbus.com/license.html)

### API End Points
 >* All buses https://ygnbus.herokuapp.com/api/bus/
 >* Each Bus https://ygnbus.herokuapp.com/api/bus/1 
 >* All Bus stops https://ygnbus.herokuapp.com/api/busstop 

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
    ]}
