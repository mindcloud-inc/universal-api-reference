# Dripcel: Search Contacts

Finds contacts in Dripcel.

```
GET https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/search-contacts?${params}`, {
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
      "data": {
        "contacts": [
          {
            "cell": "string",
            "firstname": "Ava"
          }
        ],
        "creditsUsed": 1,
        "parsedRequest": {
          "options": {
            "limit": 1,
            "skip": 1
          },
          "projection": {
            "cell": 1,
            "firstname": 1
          }
        }
      },
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.contacts[].cell` | string |  |
| `data.contacts[].firstname` | string |  |
| `data.creditsUsed` | number |  |
| `data.parsedRequest.options.limit` | number |  |
| `data.parsedRequest.options.skip` | number |  |
| `data.parsedRequest.projection.cell` | number |  |
| `data.parsedRequest.projection.firstname` | number |  |
| `ok` | boolean |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `POST /contacts/search` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

