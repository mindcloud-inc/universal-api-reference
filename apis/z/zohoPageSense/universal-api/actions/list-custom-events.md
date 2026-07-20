# Zoho PageSense: List Custom Events

Retrieves custom events from Zoho PageSense.

```
GET https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-custom-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-custom-events?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&projectLinkname=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "projectLinkname": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-custom-events?${params}`, {
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
| `portalName` | string | yes | Portal identifier in the path. |
| `projectLinkname` | string | yes | Project linkname query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "customevents": [
        {
          "eventName": "Ava Chen",
          "linkname": "https://example.com"
        }
      ],
      "statusCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `customevents[].eventName` | string |  |
| `customevents[].linkname` | string |  |
| `statusCode` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `GET /portal/:portalName/customevents` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-events.md) for the provider-specific parameters and requirements.

