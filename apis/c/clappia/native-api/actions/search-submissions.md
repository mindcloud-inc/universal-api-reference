# Search Submissions with Clappia

Finds submissions in Clappia by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/getSubmissions`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Search Submissions](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `requestingUserEmailAddress` | body | `string` | yes | Email address of the Clappia user on whose behalf submissions should be listed. |
| `pageSize` | body | `number` | no | Maximum number of submissions to return. |
| `filters` | body | `object` | no | Optional Clappia filters object for narrowing returned submissions. |
