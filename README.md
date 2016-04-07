# Travel-exercise
# Metadata<br>
fields: <br>
    - messageid :   { type: string, comment: 'Unique ID for trip bundle'}<br>
    - tripindex :   { type: integer, comment: 'Within-bundle trip count, from 0'}<br>
    - received :    { type: date, format: epoch-seconds }<br>
    - currency :    { type: string, tags: [categorical], comment: 'Convert prices via currency xref' }<br>
    - total :       { type: real }<br>
    - tax :         { type: real }<br>
    - surcharge :   { type: real }<br>
    - source :      { type: string, tags: [categorical] }<br>
    - merchant :    { type: string, tags: [categorical], comment: 'Ticketing authority' }<br>
    - majorcarrierid: {type: string, tags: [categorical], comment: 'Ticketing airline' }<br>
    - origin :      { type: string, tags: [categorical], comment: 'Three letter IATA airport code' }<br>
    - destination : { type: string, tags: [categorical], comment: 'Three letter IATA airport code' }<br>
    - departure :   { type: date, format: epoch-seconds, comment: 'UTC time of departure (convert to origin TZ to get local departure time)' }<br>
    - return :      { type: date, format: epoch-seconds, comment: 'UTC time of departure (convert to destination TZ to get local return time)' }<br>
    - los2 :         { type: integer, comment: 'Difference between yyyymmdd of departure in local time at origin and yyyymmdd of return in local time at destination.' }<br>
    - outbounddurationminutes : { type: integer }<br>
    - outboundstops : { type : integer }<br>
    - returndurationminutes : { type : integer }<br>
    - returnstops : { type : integer }<br>
    - availableseats : { type : integer }<br>
    - cabinclass : { type: string, tags: [categorical], values: [E, B, F], comment: 'Economy, business or first class' }<br>
    - paxtype : { type: string, tags: [categorical] }<br>
    - refundable : { type: boolean, comment: 'Indicates refundable ticket' }<br>
    - triptimestamp : { type: date, format: epoch-seconds, comment: 'When this query result was generated (UTC)' }<br>
    - receiveddate : { type: date, format: yyyymmdd, comment: 'Day message received at Hopper.  Hive table is partitioned on this value' }<br>
