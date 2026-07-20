# PIMMS: Retrieve Analytics

Retrieves filtered analytics metrics from PIMMS.

```
GET https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PIMMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-analytics?${params}`, {
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
| `event` | string | no | The type of event to retrieve analytics for. Defaults to `clicks`. |
| `groupBy` | string | no | The parameter to group the analytics data points by. Defaults to `count` if undefined. |
| `domain` | string | no | The domain to filter analytics for. |
| `key` | string | no | The short link slug. |
| `linkId` | string | no | The unique ID of the short link on PiMMs. |
| `externalId` | string | no | This is the ID of the link in the your database. Must be prefixed with 'ext_' when passed as a query parameter. |
| `tenantId` | string | no | The ID of the tenant that created the link inside your system. |
| `programId` | string | no | The ID of the program to retrieve analytics for. |
| `partnerId` | string | no | The ID of the partner to retrieve analytics for. |
| `interval` | string | no | The interval to retrieve analytics for. If undefined, defaults to 24h. |
| `start` | string | no | The start date and time when to retrieve analytics from. Takes precedence over `interval`. |
| `end` | string | no | The end date and time when to retrieve analytics from. If not provided, defaults to the current date. Takes precedence over `interval`. |
| `timezone` | string | no | The IANA time zone code for aligning timeseries granularity (e.g. America/New_York). Defaults to UTC. |
| `country` | string | no | The country to retrieve analytics for. |
| `city` | string | no | The city to retrieve analytics for. |
| `region` | string | no | The ISO 3166-2 region code to retrieve analytics for. |
| `continent` | string | no | The continent to retrieve analytics for. |
| `device` | string | no | The device to retrieve analytics for. |
| `browser` | string | no | The browser to retrieve analytics for. |
| `os` | string | no | The OS to retrieve analytics for. |
| `trigger` | string | no | The trigger to retrieve analytics for. If undefined, return both QR and link clicks. |
| `referer` | string | no | The referer to retrieve analytics for. |
| `refererUrl` | string | no | The full referer URL to retrieve analytics for. |
| `url` | string | no | The URL to retrieve analytics for. |
| `tagId` | string | no | Deprecated. Use `tagIds` instead. The tag ID to retrieve analytics for. |
| `tagIds` | string | no | The tag IDs to retrieve analytics for. |
| `folderId` | string | no | The folder ID to retrieve analytics for. If not provided, return analytics for unsorted links. |
| `qr` | boolean | no | Deprecated. Use the `trigger` field instead. Filter for QR code scans. If true, filter for QR codes only. If false, filter for links only. If undefined, return both. |
| `root` | boolean | no | Filter for root domains. If true, filter for domains only. If false, filter for links only. If undefined, return both. |
| `utmSource` | string | no | The UTM source of the short link. |
| `utmMedium` | string | no | The UTM medium of the short link. |
| `utmCampaign` | string | no | The UTM campaign of the short link. |
| `utmTerm` | string | no | The UTM term of the short link. |
| `utmContent` | string | no | The UTM content of the short link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "leads": 1,
      "saleAmount": 1,
      "sales": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number | Total click count for the filtered analytics window. |
| `leads` | number | Total attributed lead conversions for the filtered analytics window. |
| `saleAmount` | number | Total attributed sale amount for the filtered analytics window. |
| `sales` | number | Total attributed sales conversions for the filtered analytics window. |

## Native endpoint

Through the native PIMMS API, this operation is `GET /analytics` (base URL `https://api.pimms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-analytics.md) for the provider-specific parameters and requirements.

