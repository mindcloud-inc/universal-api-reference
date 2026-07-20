# Mighty Tix: Delete Venue

Deletes an existing venue from Mighty Tix.

```
DELETE https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-venue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-venue?connectionId=$CONNECTION_ID&variables.input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-venue?${params}`, {
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
| `variables.input` | object | yes | DeleteOneVenueInput object from the Mighty Tix Admin GraphQL docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "id": "string",
      "name": "Ava Chen",
      "space": "string",
      "timezone": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `id` | string |  |
| `name` | string |  |
| `space` | string |  |
| `timezone` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Mighty Tix API, this operation is `POST admin-api/graphql` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-venue.md) for the provider-specific parameters and requirements.

