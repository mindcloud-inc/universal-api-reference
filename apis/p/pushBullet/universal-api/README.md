# <img src="https://images.mindcloud.co/apps/icons/pushbullet_1773340379813.png" alt="Pushbullet logo" width="28" height="28"> Pushbullet: Universal API

Send, receive, and manage pushes, devices, contacts, and subscriptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pushBullet/latest
- **Category:** Communication / Team Messaging
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pushbullet.com
- **Vendor API docs:** https://docs.pushbullet.com/v8/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Info](actions/get-channel-info.md) | GET | Finds channel details in Pushbullet by channel tag. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | POST | Creates a new chat in Pushbullet. |
| [Delete Chat](actions/delete-chat.md) | DELETE | Deletes an existing chat from Pushbullet. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from your Pushbullet account. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in Pushbullet. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Create Device](actions/create-device.md) | POST | Creates a new device in Pushbullet. |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes an existing device from Pushbullet. |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from your Pushbullet account. |
| [Update Device](actions/update-device.md) | PUT | Updates an existing device in Pushbullet. |

### Ephemeral

| Action | Method | Description |
| --- | --- | --- |
| [Send Ephemeral](actions/send-ephemeral.md) | POST | Sends an ephemeral message to the Pushbullet realtime stream. |

### Push

| Action | Method | Description |
| --- | --- | --- |
| [Create Push](actions/create-push.md) | POST | Creates a new push in Pushbullet. |
| [Delete All Pushes](actions/delete-all-pushes.md) | DELETE | Deletes all pushes from your Pushbullet account. |
| [Delete Push](actions/delete-push.md) | DELETE | Deletes an existing push from Pushbullet. |
| [List Pushes](actions/list-pushes.md) | GET | Retrieves pushes from your Pushbullet account. |
| [Update Push](actions/update-push.md) | PUT | Updates an existing push in Pushbullet. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Pushbullet. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes an existing subscription from Pushbullet. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from your Pushbullet account. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload Request](actions/create-upload-request.md) | POST | Creates a file upload request in Pushbullet. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Pushbullet. |

