# HoorayHR: Get Working Today Overview

Retrieves a working today overview from HoorayHR.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-working-today-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-working-today-overview?connectionId=$CONNECTION_ID&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-working-today-overview?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes | The day to inspect in YYYY-MM-DD format. |
| `includeArchivedUsers` | boolean | no | Whether archived users should be included in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isWorkingToday": true,
      "userId": 1,
      "workLocationCategoryId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isWorkingToday` | boolean |  |
| `userId` | number |  |
| `workLocationCategoryId` | number |  |

## Native endpoint

Through the native HoorayHR API, this operation is `GET /working-today` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-working-today-overview.md) for the provider-specific parameters and requirements.

