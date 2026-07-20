# Zoho PageSense: Get Experiment Details

Retrieves experiment details from Zoho PageSense.

```
GET https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-experiment-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-experiment-details?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&experimentLinkname=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "experimentLinkname": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-experiment-details?${params}`, {
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
| `experimentLinkname` | string | yes | Experiment linkname in the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "experiments": [
        {
          "displayName": "Ava Chen",
          "experimentKey": "string",
          "experimentType": 1,
          "linkname": "https://example.com",
          "projectLinkname": "https://example.com",
          "success": true,
          "variations": [
            {
              "name": "Ava Chen",
              "trafficAllocation": 1,
              "variationId": 1,
              "variationUrl": "https://example.com"
            }
          ]
        }
      ],
      "statusCode": "string",
      "statusString": "string",
      "timeTakenToProcessTheRequest": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `experiments[].displayName` | string |  |
| `experiments[].experimentKey` | string |  |
| `experiments[].experimentType` | number |  |
| `experiments[].linkname` | string |  |
| `experiments[].projectLinkname` | string |  |
| `experiments[].success` | boolean |  |
| `experiments[].variations[].name` | string |  |
| `experiments[].variations[].trafficAllocation` | number |  |
| `experiments[].variations[].variationId` | number |  |
| `experiments[].variations[].variationUrl` | string |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `GET /portal/:portalName/experiments/:experimentLinkname` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experiment-details.md) for the provider-specific parameters and requirements.

