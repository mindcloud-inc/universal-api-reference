# Create Video OTP with VdoCipher

Creates a playback OTP in VdoCipher.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/otp`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Create Video OTP](https://www.vdocipher.com/docs/server/playbackauth/otp)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `annotate` | body | `string` | no |
| `forcedBitrate` | body | `number` | no |
| `ipGeoRules` | body | `string` | no |
| `nocdn` | body | `string` | no |
| `ttl` | body | `number` | no |
| `videoId` | path | `string` | no |
| `whitelisthref` | body | `string` | no |
