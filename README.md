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

## Property Key Case 

We have adopted the snake_case convention for all property keys within our JSON format. 

This approach ensures consistency, readability, and alignment with common JSON practices. 

The key characteristics of this naming convention are:

- Lowercase Letters: All property names use lowercase letters.

- Underscores for Separation: Words within a key are separated by underscores (_) rather than spaces or hyphens.

## Property Key Naming Standard 

In most cases, the name of the entity is included at the beginning of the property key, but not any parent entities.

For instance here, we name the property key 'deployment_country'  -  not 'country' or 'platform_deployment_country'

And we name the property key 'country_name'  -  not 'name' or 'platform_deployment_country_name'

```json
"platform_deployment": {
    "deployment_method": {},
    "deployment_country": {
        "country_code3": "DEU",
        "country_code2": "DE",
        "country_name": "Germany",
        "country_id": 164
    }
}
```