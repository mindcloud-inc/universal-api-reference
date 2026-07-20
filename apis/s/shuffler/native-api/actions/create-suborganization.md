# Create Suborganization with Shuffler

Creates a suborganization in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/{orgId}/create_sub_org`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Create Suborganization](https://shuffler.io/docs/API#create-a-suborg)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Child organization name. |
| `orgId` | path | `string` | yes | Org Id path parameter. |
