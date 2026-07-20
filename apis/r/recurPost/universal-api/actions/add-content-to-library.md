# RecurPost: Add Content to Library

Creates library content in RecurPost.

```
POST https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/add-content-to-library
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RecurPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/add-content-to-library" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/add-content-to-library', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bsMessage` | string | no |  |
| `contentExpiredate` | string | no |  |
| `contentLivedate` | string | no |  |
| `fbFirstComment` | string | no |  |
| `fbMessage` | string | no |  |
| `fbPostType` | string | no |  |
| `firstComment` | string | no |  |
| `gbpCta` | string | no |  |
| `gbpCtaUrl` | string | no |  |
| `gbpOfferCouponCode` | string | no |  |
| `gbpOfferEndDate` | string | no |  |
| `gbpOfferStartDate` | string | no |  |
| `gbpOfferTerms` | string | no |  |
| `gbpOfferTitle` | string | no |  |
| `gbpRedeemOfferLink` | string | no |  |
| `gmbMessage` | string | no |  |
| `hostImagesOnRecurpost` | boolean | no |  |
| `id` | string | yes | Library ID from List Libraries. |
| `imageUrl[]` | array<string> | no |  |
| `inFirstComment` | string | no |  |
| `inMessage` | string | no |  |
| `inPostType` | string | no |  |
| `inReelShareInFeed` | string | no |  |
| `isTopOfQueue` | number | no |  |
| `lnDocument` | string | no |  |
| `lnDocumentTitle` | string | no |  |
| `lnFirstComment` | string | no |  |
| `lnMessage` | string | no |  |
| `message` | string | yes | Default message or content for the post. |
| `piMessage` | string | no |  |
| `piTitle` | string | no |  |
| `thMessage` | string | no |  |
| `tkAllowComments` | string | no |  |
| `tkAllowDuet` | string | no |  |
| `tkAllowStitches` | string | no |  |
| `tkMessage` | string | no |  |
| `tkPrivacyStatus` | string | no |  |
| `twMessage` | string | no |  |
| `url` | string | no |  |
| `videoUrl` | string | no |  |
| `ytCategory` | string | no |  |
| `ytMessage` | string | no |  |
| `ytPrivacyStatus` | string | no |  |
| `ytThumb` | string | no |  |
| `ytTitle` | string | no |  |
| `ytUserTags` | string | no |  |
| `ytVideoMadeForKids` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native RecurPost API, this operation is `POST /api/add_content_in_library` (base URL `https://social.recurpost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-content-to-library.md) for the provider-specific parameters and requirements.

