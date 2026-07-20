# Maildrip: Verify the setup health of an opt-in page



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-the-setup-health-of-an-opt-in-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-the-setup-health-of-an-opt-in-page?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-the-setup-health-of-an-opt-in-page?${params}`, {
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
| `pageId` | string | yes | ID of the opt-in page to verify |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allGroupsExist": true,
      "campaignLinkedGroupCount": 1,
      "groupCount": 1,
      "hasCampaign": true,
      "hasContactGroups": true,
      "healthy": true,
      "missingGroupCount": 1,
      "published": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allGroupsExist` | boolean | True when every referenced group ID resolves to an existing ContactGroup document |
| `campaignLinkedGroupCount` | number |  |
| `groupCount` | number | Number of contact group IDs listed on this page |
| `hasCampaign` | boolean | At least one linked group has a campaign |
| `hasContactGroups` | boolean | At least one contact group is configured |
| `healthy` | boolean | True only if the page is published, has contact groups, all groups exist, and at least one group has a campaign |
| `missingGroupCount` | number | Number of referenced groups that no longer exist in the database |
| `published` | boolean |  |
| `warnings` | array<string> | Human-readable warning messages |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/opt-in-pages/{pageId}/verify-setup` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-the-setup-health-of-an-opt-in-page.md) for the provider-specific parameters and requirements.

