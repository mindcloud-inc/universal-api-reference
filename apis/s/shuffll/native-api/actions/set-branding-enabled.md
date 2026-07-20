# Set Branding Enabled with Shuffll

Updates branding settings in Shuffll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/auth/branding/entity`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Set Branding Enabled](https://api-docs.shuffll.com/apis/branding/updatebranding)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | body | `object` | no | Target organization object when no workspace is provided. Pass an object with an id field. |
| `propertyValue` | body | `boolean` | yes | New value for the selected branding property when updating boolean fields like enabled. |
| `workspace` | body | `object` | no | Target workspace object. Pass an object with an id field. |
