# Netlify: Get DNS for Site



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-dns-for-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-dns-for-site?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-dns-for-site?${params}`, {
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
| `siteId` | list<string> | yes | The Netlify site ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "accountSlug": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dedicated": true,
      "dnsServers": [
        "string"
      ],
      "domain": "string",
      "errors": [
        "string"
      ],
      "id": "string",
      "ipv6Enabled": true,
      "name": "Ava Chen",
      "records": [
        {
          "dnsZoneId": "string",
          "flag": 1,
          "hostname": "Ava Chen",
          "id": "string",
          "managed": true,
          "priority": 1,
          "siteId": "string",
          "tag": "string",
          "ttl": 1,
          "type": "string",
          "value": "string"
        }
      ],
      "siteId": "string",
      "supportedRecordTypes": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountName` | string |  |
| `accountSlug` | string |  |
| `createdAt` | date |  |
| `dedicated` | boolean |  |
| `dnsServers[]` | string |  |
| `domain` | string |  |
| `errors[]` | string |  |
| `id` | string |  |
| `ipv6Enabled` | boolean |  |
| `name` | string |  |
| `records[].dnsZoneId` | string |  |
| `records[].flag` | number |  |
| `records[].hostname` | string |  |
| `records[].id` | string |  |
| `records[].managed` | boolean |  |
| `records[].priority` | number |  |
| `records[].siteId` | string |  |
| `records[].tag` | string |  |
| `records[].ttl` | number |  |
| `records[].type` | string |  |
| `records[].value` | string |  |
| `siteId` | string |  |
| `supportedRecordTypes[]` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Netlify API, this operation is `GET /sites/:site_id/dns` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dns-for-site.md) for the provider-specific parameters and requirements.

