# Search Group Members with Explara

Finds group members in Explara by keyword or email.

## Endpoint

- **Method:** `POST`
- **Path:** `/cm/api/publisher/search-members`
- **Base URL:** `https://www.explara.com`
- **Official documentation:** [Search Group Members](https://apidocs.explara.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Explara group identifier. |
| `status` | body | `string` | no | Membership status filter, such as active or expired. |
