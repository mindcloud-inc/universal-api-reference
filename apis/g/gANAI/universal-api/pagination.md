# GAN.AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GAN.AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-avatar-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GAN.AI actions that support pagination

- [List Avatar Videos](actions/list-avatar-videos.md)
- [List Avatars](actions/list-avatars.md)
- [List Photo Avatar Inferences](actions/list-photo-avatar-inferences.md)
- [List Photo Avatars](actions/list-photo-avatars.md)
- [List Sound Effect History](actions/list-sound-effect-history.md)
- [List Text to Speech History](actions/list-text-to-speech-history.md)
- [List User LipSyncs](actions/list-user-lip-syncs.md)
