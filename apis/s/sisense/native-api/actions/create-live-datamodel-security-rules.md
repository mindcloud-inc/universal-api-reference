# Create Live Datamodel Security Rules with Sisense

Creates live datamodel security rules in Sisense.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/elasticubes/live/:title/datasecurity`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Create Live Datamodel Security Rules](https://developer.sisense.com/guides/restApi/data-security.html#endpoints-2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | path | `string` | yes |
| `fullname` | body | `string` | yes |
| `table` | body | `string` | yes |
| `column` | body | `string` | yes |
| `datatype` | body | `string` | yes |
| `allMembers` | body | `boolean` | yes |
| `shares[0].partyId` | body | `string` | yes |
| `shares[0].type` | body | `string` | yes |
