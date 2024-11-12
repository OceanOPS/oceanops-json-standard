# OceanJSON

An integrated GOOS metadata JSON standard format.

## Goals

Facilitate integration and ensure seamless metadata exchange between nodes.

## Entities

The format is broken down into Key Entities (Platform, Ship, Cruise, Contact, Site, Observation, Telecom, Status, Agency, ..) each with their own schema.

## Validation

JSON Schema files for each key entity in /schemas directory.

## Examples

Sample JSON files showing how a complete JSON document would look when adhering to your format in /examples directory.
Alternatively, fetch a platform sample array from the OceanOPS API in OceanJSON format:
https://www.ocean-ops.org/api/data/oceanjson/platforms?page=1&pageSize=30&fields=ref,status,observingNetworks,programName
You can use [OceanUI](https://www.ocean-ops.org/ui) to
 help build the URL for this request, to include the filters and fields you want. 
 To do so in OceanUI, navigate to the Platforms table view, select colums, sorting options and any filters ypou like, the click Export > OceanJSON permalink, and copy the URL.

## Property Key Case 

We have adopted the snake_case convention for all property keys within our JSON format. 

This approach ensures consistency, readability, and alignment with common JSON practices. 

The key characteristics of this naming convention are:

- Lowercase Letters: All property names use lowercase letters.

- Underscores for Separation: Words within a key are separated by underscores (_) rather than spaces or hyphens.

## Property Key Naming Standard 

In almost all cases, we avoid prefixing the name of the entity in the property key.

For instance here, we name the property key 'country'  -  not 'deployment_country' or 'platform_deployment_country'

And we name the property key 'name'  -  not 'country_name' or 'platform_deployment_country_name'

```json
"deployment": {
    "method": {},
    "country": {
        "code3": "DEU",
        "code2": "DE",
        "name": "Germany",
        "id": 164
    }
}
```
