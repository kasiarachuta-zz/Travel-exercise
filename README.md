# Travel-exercise
# Metadata
fields:
    - messageid :   { type: string, comment: 'Unique ID for trip bundle'}
    - tripindex :   { type: integer, comment: 'Within-bundle trip count, from 0'}
    - received :    { type: date, format: epoch-seconds }
    - currency :    { type: string, tags: [categorical], comment: 'Convert prices via currency xref' }
    - total :       { type: real }
    - tax :         { type: real }
    - surcharge :   { type: real }
    - source :      { type: string, tags: [categorical] }
    - merchant :    { type: string, tags: [categorical], comment: 'Ticketing authority' }
    - majorcarrierid: {type: string, tags: [categorical], comment: 'Ticketing airline' }
    - origin :      { type: string, tags: [categorical], comment: 'Three letter IATA airport code' }
    - destination : { type: string, tags: [categorical], comment: 'Three letter IATA airport code' }
    - departure :   { type: date, format: epoch-seconds, comment: 'UTC time of departure (convert to origin TZ to get local departure time)' }
    - return :      { type: date, format: epoch-seconds, comment: 'UTC time of departure (convert to destination TZ to get local return time)' }
    - los2 :         { type: integer, comment: 'Difference between yyyymmdd of departure in local time at origin and yyyymmdd of return in local time at destination.' }
    - outbounddurationminutes : { type: integer }
    - outboundstops : { type : integer }
    - returndurationminutes : { type : integer }
    - returnstops : { type : integer }
    - availableseats : { type : integer }
    - cabinclass : { type: string, tags: [categorical], values: [E, B, F], comment: 'Economy, business or first class' }
    - paxtype : { type: string, tags: [categorical] }
    - refundable : { type: boolean, comment: 'Indicates refundable ticket' }
    - triptimestamp : { type: date, format: epoch-seconds, comment: 'When this query result was generated (UTC)' }
    - receiveddate : { type: date, format: yyyymmdd, comment: 'Day message received at Hopper.  Hive table is partitioned on this value' }
