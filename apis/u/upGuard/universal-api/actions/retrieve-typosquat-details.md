# UpGuard: Retrieve Typosquat Details

Retrieves typosquat details for a domain in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-typosquat-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-typosquat-details?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-typosquat-details?${params}`, {
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
| `domain` | string | yes | The domain for which to return typosquat details |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ignored": [
        {
          "aRecords": [
            "string"
          ],
          "country": "string",
          "hostname": "Ava Chen",
          "mxRecords": [
            "string"
          ],
          "nsRecords": [
            "string"
          ],
          "permutationType": "string"
        }
      ],
      "registered": [
        {
          "aRecords": [
            "string"
          ],
          "country": "string",
          "dateDetected": "string",
          "hostname": "Ava Chen",
          "nsRecords": [
            "string"
          ],
          "permutationType": "string"
        }
      ],
      "unregistered": [
        {
          "hostname": "Ava Chen",
          "permutationType": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ignored[].aRecords[]` | string |  |
| `ignored[].country` | string |  |
| `ignored[].hostname` | string |  |
| `ignored[].mxRecords[]` | string |  |
| `ignored[].nsRecords[]` | string |  |
| `ignored[].permutationType` | string |  |
| `registered[].aRecords[]` | string |  |
| `registered[].country` | string |  |
| `registered[].dateDetected` | string |  |
| `registered[].hostname` | string |  |
| `registered[].nsRecords[]` | string |  |
| `registered[].permutationType` | string |  |
| `unregistered[].hostname` | string |  |
| `unregistered[].permutationType` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /typosquat/details` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-typosquat-details.md) for the provider-specific parameters and requirements.

