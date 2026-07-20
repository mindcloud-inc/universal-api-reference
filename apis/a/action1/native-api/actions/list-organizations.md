# List Organizations with Action1

Retrieves organizations from the current Action1 enterprise.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Organizations](https://app.action1.com/apidocs/#/Security.%20Organization%20Object/organizations_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `admin` | query | `string` | no | Specify 'yes' to get all organizations where the current user is at least an organization admin. |
