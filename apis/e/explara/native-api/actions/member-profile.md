# Member Profile with Explara

Retrieves a member profile from Explara.

## Endpoint

- **Method:** `POST`
- **Path:** `/cm/api/publisher/public-profile`
- **Base URL:** `https://www.explara.com`
- **Official documentation:** [Member Profile](https://apidocs.explara.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Explara group identifier for the member profile lookup. |
| `memberId` | body | `string` | yes | Explara member identifier for the member profile lookup. |
