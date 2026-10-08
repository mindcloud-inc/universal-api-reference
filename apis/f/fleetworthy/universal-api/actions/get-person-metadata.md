# Fleetworthy: Get Person Metadata



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "regulatedDocumentStatuses": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `regulatedDocumentStatuses` | array<object> | Available regulated-document statuses. |

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /people/metadata` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-metadata.md) for the provider-specific parameters and requirements.

