# Bitly: List Group Bitlinks

Retrieves bitlinks for a group in Bitly.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-bitlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-bitlinks?connectionId=$CONNECTION_ID&groupGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-bitlinks?${params}`, {
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
| `archived` | string | no | Filter archived bitlinks. |
| `campaignGuid` | string | no | Filter results to one campaign GUID. |
| `channelGuid` | string | no | Filter results to one channel GUID. |
| `createdAfter` | string | no | Filter to bitlinks created after this epoch timestamp. |
| `createdBefore` | string | no | Filter to bitlinks created before this epoch timestamp. |
| `customBitlink` | string | no | Filter custom bitlinks. |
| `deeplinks` | string | no | Filter bitlinks by deeplink status. |
| `domainDeeplinks` | string | no | Filter bitlinks by domain deeplink status. |
| `encodingLogin[]` | array<string> | no | Filter results by encoding login values. |
| `groupGuid` | string | yes | The Bitly group GUID. |
| `hasQrCodes` | string | no | Filter bitlinks by QR code presence. |
| `hostnamePathQuery` | string | no | Filter by hostname, path, or query text. |
| `launchpadIds[]` | array<string> | no | Filter results by launchpad IDs. |
| `query` | string | no | Search bitlinks by query text. |
| `searchAfter` | string | no | Token used to request the next batch of results. |
| `size` | number | no | The number of bitlinks to return. |
| `tags[]` | array<string> | no | Filter results by tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        {
          "archived": true,
          "clientId": "https://example.com",
          "createdAt": "https://example.com",
          "createdBy": "https://example.com",
          "id": "https://example.com",
          "link": "https://example.com",
          "longUrl": "https://example.com",
          "references": {
            "group": "https://example.com"
          },
          "title": "https://example.com"
        }
      ],
      "pagination": {
        "next": "string",
        "searchAfter": "string",
        "size": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links[].archived` | boolean |  |
| `links[].clientId` | string |  |
| `links[].createdAt` | string |  |
| `links[].createdBy` | string |  |
| `links[].id` | string |  |
| `links[].link` | string |  |
| `links[].longUrl` | string |  |
| `links[].references.group` | string |  |
| `links[].title` | string |  |
| `pagination.next` | string |  |
| `pagination.searchAfter` | string |  |
| `pagination.size` | number |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /groups/:group_guid/bitlinks` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-bitlinks.md) for the provider-specific parameters and requirements.

