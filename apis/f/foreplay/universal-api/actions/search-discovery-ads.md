# Foreplay: Search Discovery Ads

Finds ads in Foreplay's discovery index.

```
GET https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/search-discovery-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foreplay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/search-discovery-ads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/search-discovery-ads?${params}`, {
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
      "ad_id": "string",
      "avatar": "string",
      "brand_id": "string",
      "cards": [
        {
          "cta_text": "string",
          "description": "string",
          "headline": "string",
          "image": "string",
          "link_description": "https://example.com",
          "title": "string",
          "type": "string",
          "video": "string",
          "video_duration": 1
        }
      ],
      "categories": [
        "string"
      ],
      "content_filter": {
        "Before_and_After": 1,
        "Facts_and_Stats": 1,
        "Features_and_Benefits": 1,
        "Green_Screen": 1,
        "Holiday_Seasonal": 1,
        "Media_and_Press": 1,
        "other": 1,
        "Podcast": 1,
        "Promotion_and_Discount": 1,
        "Reasons_why": 1,
        "Testimonial_Review": 1,
        "UGC": 1,
        "Unboxing": 1,
        "Us_vs_Them": 1
      },
      "creative_targeting": "string",
      "cta_title": "string",
      "cta_type": "string",
      "description": "string",
      "display_format": "string",
      "emotional_drivers": {
        "achievement": 1,
        "anger": 1,
        "authority": 1,
        "belonging": 1,
        "competence": 1,
        "curiosity": 1,
        "empowerment": 1,
        "engagement": 1,
        "esteem": 1,
        "fear": 1,
        "guilt": 1,
        "nostalgia": 1,
        "nurturance": 1,
        "security": 1,
        "urgency": 1
      },
      "full_transcription": "string",
      "headline": "string",
      "id": "string",
      "image": "string",
      "languages": [
        "string"
      ],
      "link_url": "https://example.com",
      "live": true,
      "market_target": "string",
      "name": "Ava Chen",
      "niches": [
        "string"
      ],
      "persona": {
        "age": "string",
        "gender": "string"
      },
      "product_category": "string",
      "publisher_platform": [
        "string"
      ],
      "running_duration": {
        "days": 1,
        "hours": 1,
        "minutes": 1,
        "seconds": 1
      },
      "started_running": 1,
      "thumbnail": "string",
      "time_product_was_mentioned": 1,
      "timestamped_transcription": [
        {
          "endTime": 1,
          "sentence": "string",
          "startTime": 1
        }
      ],
      "type": "string",
      "video": "string",
      "video_duration": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ad_id` | string |  |
| `avatar` | string |  |
| `brand_id` | string |  |
| `cards[].cta_text` | string |  |
| `cards[].description` | string |  |
| `cards[].headline` | string |  |
| `cards[].image` | string |  |
| `cards[].link_description` | string |  |
| `cards[].title` | string |  |
| `cards[].type` | string |  |
| `cards[].video` | string |  |
| `cards[].video_duration` | number |  |
| `categories[]` | string |  |
| `content_filter.Before_and_After` | number |  |
| `content_filter.Facts_and_Stats` | number |  |
| `content_filter.Features_and_Benefits` | number |  |
| `content_filter.Green_Screen` | number |  |
| `content_filter.Holiday_Seasonal` | number |  |
| `content_filter.Media_and_Press` | number |  |
| `content_filter.other` | number |  |
| `content_filter.Podcast` | number |  |
| `content_filter.Promotion_and_Discount` | number |  |
| `content_filter.Reasons_why` | number |  |
| `content_filter.Testimonial_Review` | number |  |
| `content_filter.UGC` | number |  |
| `content_filter.Unboxing` | number |  |
| `content_filter.Us_vs_Them` | number |  |
| `creative_targeting` | string |  |
| `cta_title` | string |  |
| `cta_type` | string |  |
| `description` | string |  |
| `display_format` | string |  |
| `emotional_drivers.achievement` | number |  |
| `emotional_drivers.anger` | number |  |
| `emotional_drivers.authority` | number |  |
| `emotional_drivers.belonging` | number |  |
| `emotional_drivers.competence` | number |  |
| `emotional_drivers.curiosity` | number |  |
| `emotional_drivers.empowerment` | number |  |
| `emotional_drivers.engagement` | number |  |
| `emotional_drivers.esteem` | number |  |
| `emotional_drivers.fear` | number |  |
| `emotional_drivers.guilt` | number |  |
| `emotional_drivers.nostalgia` | number |  |
| `emotional_drivers.nurturance` | number |  |
| `emotional_drivers.security` | number |  |
| `emotional_drivers.urgency` | number |  |
| `full_transcription` | string |  |
| `headline` | string |  |
| `id` | string |  |
| `image` | string |  |
| `languages[]` | string |  |
| `link_url` | string |  |
| `live` | boolean |  |
| `market_target` | string |  |
| `name` | string |  |
| `niches[]` | string |  |
| `persona.age` | string |  |
| `persona.gender` | string |  |
| `product_category` | string |  |
| `publisher_platform[]` | string |  |
| `running_duration.days` | number |  |
| `running_duration.hours` | number |  |
| `running_duration.minutes` | number |  |
| `running_duration.seconds` | number |  |
| `started_running` | number |  |
| `thumbnail` | string |  |
| `time_product_was_mentioned` | number |  |
| `timestamped_transcription[].endTime` | number |  |
| `timestamped_transcription[].sentence` | string |  |
| `timestamped_transcription[].startTime` | number |  |
| `type` | string |  |
| `video` | string |  |
| `video_duration` | number |  |

## Native endpoint

Through the native Foreplay API, this operation is `GET /api/discovery/ads` (base URL `https://public.api.foreplay.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-discovery-ads.md) for the provider-specific parameters and requirements.

