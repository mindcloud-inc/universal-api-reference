# <img src="https://images.mindcloud.co/apps/icons/id-qv4g3gyt-1773165879166_1773165889131.png" alt="Twitch logo" width="28" height="28"> Twitch: Universal API

Manage channels, schedules, polls, clips, and stream settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/twitch/latest
- **Category:** Marketing / Social Media
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.twitch.tv
- **Vendor API docs:** https://dev.twitch.tv/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Channel Stream Schedule](actions/get-channel-stream-schedule.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-channel-stream-schedule?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Games](actions/list-games.md) | GET | Retrieves game category records from Twitch. |
| [List Top Games](actions/list-top-games.md) | GET | Retrieves top game categories from Twitch. |
| [Search Categories](actions/search-categories.md) | GET | Searches Twitch categories using a query. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Followed Channels](actions/list-followed-channels.md) | GET | Retrieves followed channels for a user from Twitch. |
| [Modify Channel Information](actions/modify-channel-information.md) | PUT | Updates broadcaster channel information in Twitch. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat Settings](actions/get-chat-settings.md) | GET | Retrieves channel chat settings from Twitch. |
| [Get Stream Key](actions/get-stream-key.md) | GET | Retrieves a stream key from Twitch. |
| [List Channel Emotes](actions/list-channel-emotes.md) | GET | Retrieves channel emote records from Twitch. |
| [List Channel Information](actions/list-channel-information.md) | GET | Retrieves broadcaster channel information from Twitch. |
| [Search Channels](actions/search-channels.md) | GET | Searches Twitch channels using a query. |
| [Update Chat Settings](actions/update-chat-settings.md) | PUT | Updates channel chat settings in Twitch. |

### Chatter

| Action | Method | Description |
| --- | --- | --- |
| [List Chatters](actions/list-chatters.md) | GET | Retrieves channel chatter records from Twitch. |

### Clip

| Action | Method | Description |
| --- | --- | --- |
| [Create Clip](actions/create-clip.md) | POST | Creates a new clip in Twitch. |

### Engagements

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Rewards](actions/create-custom-rewards.md) | POST | Creates a custom reward in Twitch. |
| [Create Prediction](actions/create-prediction.md) | POST | Creates a new prediction in Twitch. |
| [Delete Custom Reward](actions/delete-custom-reward.md) | DELETE | Deletes a custom reward from Twitch. |
| [End Prediction](actions/end-prediction.md) | PUT | Ends an existing prediction in Twitch. |
| [List Custom Rewards](actions/list-custom-rewards.md) | GET | Retrieves custom reward records from Twitch. |

### Poll

| Action | Method | Description |
| --- | --- | --- |
| [Create Poll](actions/create-poll.md) | POST | Creates a new poll in Twitch. |
| [End Poll](actions/end-poll.md) | PUT | Ends an existing poll in Twitch. |
| [List Polls](actions/list-polls.md) | GET | Retrieves broadcaster poll records from Twitch. |

### Prediction

| Action | Method | Description |
| --- | --- | --- |
| [List Predictions](actions/list-predictions.md) | GET | Retrieves broadcaster prediction records from Twitch. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [List Clips](actions/list-clips.md) | GET | Retrieves clip records and metadata from Twitch. |
| [List Videos](actions/list-videos.md) | GET | Retrieves video records and metadata from Twitch. |

### Schedule Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel Stream Schedule Segment](actions/create-channel-stream-schedule-segment.md) | POST | Creates a stream schedule segment in Twitch. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Stream Schedule](actions/get-channel-stream-schedule.md) | GET | Retrieves channel stream schedules from Twitch. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Delete Channel Stream Schedule Segment](actions/delete-channel-stream-schedule-segment.md) | DELETE | Deletes a stream schedule segment from Twitch. |
| [Update Channel Stream Schedule Segment](actions/update-channel-stream-schedule-segment.md) | PUT | Updates a stream schedule segment in Twitch. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [List Followed Streams](actions/list-followed-streams.md) | GET | Retrieves followed live streams from Twitch. |
| [List Streams](actions/list-streams.md) | GET | Retrieves live stream records from Twitch. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves user profiles and metadata from Twitch. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Editors](actions/list-channel-editors.md) | GET | Retrieves channel editor records from Twitch. |
| [List Channel Followers](actions/list-channel-followers.md) | GET | Retrieves channel follower records from Twitch. |

