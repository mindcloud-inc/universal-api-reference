# Create Datasource with Instasent

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project/datasource`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Create Datasource](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `name` | body | `string` | yes | Datasource name. |
| `description` | body | `string` | no | Datasource description. |
| `audienceTags[]` | body | `array<string>` | yes | Audience tags to assign to the datasource. |
| `tags[]` | body | `array<string>` | no | Datasource tags. |
| `defaultCountry` | body | `string` | no | Default country code for contacts. |
| `locale` | body | `string` | no | Datasource locale. |
| `timezone` | body | `string` | no | Datasource timezone. |
