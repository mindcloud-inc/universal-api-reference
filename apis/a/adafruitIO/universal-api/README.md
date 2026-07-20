# <img src="https://images.mindcloud.co/apps/icons/adafruit-io_1774536426442.png" alt="Adafruit IO logo" width="28" height="28"> Adafruit IO: Universal API

Adafruit IO HTTP API wrapper for feeds, data, groups, webhooks, dashboards, permissions, users, tokens, actions, and blocks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/adafruitIO/latest
- **Category:** Content & Files / Storage
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://io.adafruit.com/
- **Vendor API docs:** https://io.adafruit.com/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Token](actions/create-token.md) | POST | Creates an access token in Adafruit IO. |
| [Delete Token](actions/delete-token.md) | DELETE | Deletes an access token from Adafruit IO. |
| [Get Token](actions/get-token.md) | GET | Retrieves an access token from Adafruit IO. |
| [List Tokens](actions/list-tokens.md) | GET | Retrieves access tokens from Adafruit IO. |

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new action in Adafruit IO. |
| [Delete Action](actions/delete-action.md) | DELETE | Deletes an action from Adafruit IO. |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from Adafruit IO. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from Adafruit IO. |
| [Replace Action](actions/replace-action.md) | PUT | Replaces an action in Adafruit IO. |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Feed](actions/create-feed.md) | POST | Creates a new feed in Adafruit IO. |
| [Create Feed in a Group](actions/create-feed-in-a-group.md) | POST | Creates a feed in an Adafruit IO group. |
| [Delete Feed](actions/delete-feed.md) | DELETE | Deletes a feed from Adafruit IO. |
| [Get Feed](actions/get-feed.md) | GET | Retrieves a feed from Adafruit IO. |
| [List Feeds](actions/list-feeds.md) | GET | Retrieves feeds from Adafruit IO. |
| [List Group Feeds](actions/list-group-feeds.md) | GET | Retrieves feeds from an Adafruit IO group. |
| [Update Feed](actions/update-feed.md) | PUT | Updates an existing feed in Adafruit IO. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Chart Feed Data](actions/chart-feed-data.md) | GET | Retrieves charted data from an Adafruit IO feed. |
| [Create Data](actions/create-data.md) | POST | Creates a data point in an Adafruit IO feed. |
| [Create Multiple Data Records](actions/create-multiple-data-records.md) | POST | Creates multiple data points in an Adafruit IO feed. |
| [Delete Data Point](actions/delete-data-point.md) | DELETE | Deletes a data point from an Adafruit IO feed. |
| [Get Data Point](actions/get-data-point.md) | GET | Retrieves a data point from an Adafruit IO feed. |
| [Get First Data](actions/get-first-data.md) | GET | Retrieves the first data point from an Adafruit IO feed. |
| [Get Last Data](actions/get-last-data.md) | GET | Retrieves the last data point from an Adafruit IO feed. |
| [Get Most Recent Data](actions/get-most-recent-data.md) | GET | Retrieves the most recent feed data from Adafruit IO in CSV format. |
| [Get Next Data](actions/get-next-data.md) | GET | Retrieves the next data point from an Adafruit IO feed. |
| [Get Previous Data](actions/get-previous-data.md) | GET | Retrieves the previous data point from an Adafruit IO feed. |
| [List Feed Data](actions/list-feed-data.md) | GET | Retrieves data points from an Adafruit IO feed. |
| [Update Data Point](actions/update-data-point.md) | PUT | Updates a data point in an Adafruit IO feed. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Send Arbitrary Data via Webhook](actions/send-arbitrary-data-via-webhook.md) | POST | Sends raw feed data to Adafruit IO via webhook. |
| [Send Data via Webhook](actions/send-data-via-webhook.md) | POST | Creates a data point in Adafruit IO via webhook. |
| [Send Notification via Webhook](actions/send-notification-via-webhook.md) | POST | Sends a notification to Adafruit IO via webhook. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Feed to Group](actions/add-feed-to-group.md) | PUT | Adds a feed to an Adafruit IO group. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Adafruit IO. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes a group from Adafruit IO. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Adafruit IO. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Adafruit IO. |
| [Remove Feed from Group](actions/remove-feed-from-group.md) | DELETE | Removes a feed from an Adafruit IO group. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Adafruit IO. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Detailed User Info](actions/get-detailed-user-info.md) | GET | Retrieves detailed user throttle info from Adafruit IO. |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user info from Adafruit IO. |

