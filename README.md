# OneLiveHackathon
Repository for One Live Hackathon 2022 project

## How to add a new provider

1. Map provider JSON result to unified format

```
id => id
name => name
address => entrances[0].address
latitude => entrances[0].latitude
longitude => entrances[0].longitude
distance.km => distance.km
distance.walking => distance.walking
cover_image => image.medium
provider => should be added by the API gateway
```

2. TBD
