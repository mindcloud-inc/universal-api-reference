# Update Response Template with Reamaze

## Endpoint

- **Method:** `PUT`
- **Path:** `/response_templates/:slug`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Update Response Template](https://www.reamaze.com/api/put_response_template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Path parameter for slug. |
| `response_template` | body | `object` | no | Body payload field documented on https://www.reamaze.com/api/put_response_template. |
