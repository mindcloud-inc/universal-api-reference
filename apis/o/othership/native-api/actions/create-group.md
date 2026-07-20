# Create Group with Othership

Creates a new group in Othership.

## Endpoint

- **Method:** `POST`
- **Path:** `/Groups`
- **Base URL:** `https://hwms-api.othership.com/api/v1/azure/scim`
- **Official documentation:** [Create Group](https://www.ietf.org/rfc/rfc7644)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | The SCIM group display name. |
| `externalId` | body | `string` | no | Provisioning-domain identifier used to correlate the group across systems. |
