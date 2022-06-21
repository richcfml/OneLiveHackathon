# OneLiveHackathon
Repository for One Live Hackathon 2022 project

## How to add a new provider

1. Map provider locations data to unified format. Example:

```
id => provider key + '-' + id (example: pk-139)
name => name
address => entrances[0].address
latitude => entrances[0].latitude
longitude => entrances[0].longitude
cover_image => image.medium
```

2. Map provider availability data to unified format. Example:

```
id => provider key + '-' + id (example: pk-139)
available => available
count => 0
```

3. Map provider rates data to unified format. Example:

```
id => rate_id
location_id => provider key + '-' + parking_id (example: pk-139)
price => parking_rate (should be the smallest currency unit = INT)
currency => 'EUR' in case of parkimeter, 'USD' in case of parkmobile
vehicle_types => vehicle_types
access_type => access_type
description => description
```

List of possible vehicle_types:

```
PARKIMETER - PARKMOBILE
car        = vehicle
motorcycle = motorcycle
van        = n/a
n/a        = oversized
```

List of possible access_type:

```
PARKIMETER - PARKMOBILE
onepass    = onepass     (booking is over after stop_time or after the vehicle leaves)
multipass  = n/a         (booking is over after stop_time)
```
