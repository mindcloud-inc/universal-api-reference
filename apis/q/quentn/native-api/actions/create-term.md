# Create Term with Quentn

## Endpoint

- **Method:** `POST`
- **Path:** `/terms`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Create Term](https://help.quentn.com/hc/en-150/articles/4518012188945-Terms-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the term. |
| `name` | body | `string` | yes | The name of the Quentn term to create. |
