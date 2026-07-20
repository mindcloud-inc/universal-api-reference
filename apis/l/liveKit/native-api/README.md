# LiveKit: Native API Reference

A consolidated summary of LiveKit's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.livekit.io/reference/server/server-apis
- **API base URL:** `{livekitUrl}`

## Authentication

### API key and secret

Use a LiveKit project URL, API key, and API secret. MindCloud signs a short-lived JWT bearer token for each Server API request.

### Credentials

- **API Key:** `apiKey` · required · Your LiveKit project API key.
- **LiveKit HTTPS API URL:** `livekitUrl` · required · Your LiveKit HTTPS API URL, for example https://example.livekit.cloud. Do not use the wss:// SDK/WebSocket URL for Server API actions.
- **API Secret:** `apiSecret` · required · Your LiveKit project API secret. Used only to sign request JWTs.
- **S3 Access Key:** `s3AccessKey` · optional · Optional AWS access key for LiveKit egress test outputs.
- **S3 Region:** `s3Region` · optional · Optional AWS region for LiveKit egress test outputs.
- **S3 Bucket:** `s3Bucket` · optional · Optional S3 bucket for LiveKit egress test outputs.

[Official authentication documentation](https://docs.livekit.io/reference/server/server-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ingress](actions/create-ingress.md) | `POST /twirp/livekit.Ingress/CreateIngress` | [docs](https://docs.livekit.io/reference/other/ingress/api/#createingress) |
| [Create Room](actions/create-room.md) | `POST /twirp/livekit.RoomService/CreateRoom` | [docs](https://docs.livekit.io/reference/other/roomservice-api/#createroom) |
| [Delete Ingress](actions/delete-ingress.md) | `POST /twirp/livekit.Ingress/DeleteIngress` | [docs](https://docs.livekit.io/reference/other/ingress/api/#deleteingress) |
| [Delete Room](actions/delete-room.md) | `POST /twirp/livekit.RoomService/DeleteRoom` | [docs](https://docs.livekit.io/reference/other/roomservice-api/#deleteroom) |
| [List Ingresses](actions/list-ingresses.md) | `POST /twirp/livekit.Ingress/ListIngress` | [docs](https://docs.livekit.io/reference/other/ingress/api/#listingress) |
| [List Participants](actions/list-participants.md) | `POST /twirp/livekit.RoomService/ListParticipants` | [docs](https://docs.livekit.io/reference/other/roomservice-api/#listparticipants) |
| [List Rooms](actions/list-rooms.md) | `POST /twirp/livekit.RoomService/ListRooms` | [docs](https://docs.livekit.io/reference/other/roomservice-api/#listrooms) |
| [Send Data](actions/send-data.md) | `POST /twirp/livekit.RoomService/SendData` | [docs](https://docs.livekit.io/reference/other/roomservice-api/#senddata) |
| [Update Ingress](actions/update-ingress.md) | `POST /twirp/livekit.Ingress/UpdateIngress` | [docs](https://docs.livekit.io/reference/other/ingress/api/#updateingress) |
| [Update Room Metadata](actions/update-room-metadata.md) | `POST /twirp/livekit.RoomService/UpdateRoomMetadata` | [docs](https://docs.livekit.io/reference/other/roomservice-api/#updateroommetadata) |
