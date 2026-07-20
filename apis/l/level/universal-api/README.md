# <img src="https://images.mindcloud.co/apps/icons/level-icon_1775828974507.png" alt="Level logo" width="28" height="28"> Level: Universal API

Level helps security teams manage devices, groups, tags, alerts, automations, and custom fields through the Level REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/level/latest
- **Category:** IT Operations / Observability
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://level.io/
- **Vendor API docs:** https://levelapi.readme.io/reference/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves a list of alerts from Level. |
| [Resolve Alert](actions/resolve-alert.md) | PUT | Resolves an active alert in Level. |
| [Show Alert](actions/show-alert.md) | GET | Retrieves an existing alert from Level. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in Level. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from Level. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves a list of custom fields from Level. |
| [Show Custom Field](actions/show-custom-field.md) | GET | Retrieves an existing custom field from Level. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in Level. |

### Custom Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Delete Custom Field Value](actions/delete-custom-field-value.md) | DELETE | Deletes a custom field value from Level. |
| [List Custom Field Values](actions/list-custom-field-values.md) | GET | Retrieves custom field values from Level. |
| [Update Custom Field Value](actions/update-custom-field-value.md) | PUT | Updates a custom field value in Level. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes an existing device from Level. |
| [List Devices](actions/list-devices.md) | GET | Retrieves a list of devices from Level. |
| [Show Device](actions/show-device.md) | GET | Retrieves an existing device from Level. |
| [Update Device](actions/update-device.md) | PUT | Updates an existing device in Level. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Assign Devices to Group](actions/assign-devices-to-group.md) | PUT | Assigns devices to a group in Level. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Level. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Level. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from Level. |
| [Remove Devices from Group](actions/remove-devices-from-group.md) | DELETE | Removes devices from a group in Level. |
| [Show Group](actions/show-group.md) | GET | Retrieves an existing group from Level. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Level. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Level. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Level. |
| [List Tags](actions/list-tags.md) | GET | Retrieves a list of tags from Level. |
| [Remove Tag from Devices](actions/remove-tag-from-devices.md) | DELETE | Removes a tag from devices in Level. |
| [Show Tag](actions/show-tag.md) | GET | Retrieves an existing tag from Level. |
| [Tag Devices](actions/tag-devices.md) | PUT | Applies a tag to devices in Level. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Level. |

### Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Webhook](actions/trigger-webhook.md) | PUT | Triggers an automation webhook in Level. |

