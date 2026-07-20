# Update User Information with WaniKani

Updates user information in WaniKani.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Update User Information](https://docs.api.wanikani.com/20170710/#update-user-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user.preferences.extra_study_autoplay_audio` | body | `boolean` | no | Automatically play pronunciation audio for vocabulary during extra study. |
| `user.preferences.lessons_autoplay_audio` | body | `boolean` | no | Automatically play pronunciation audio for vocabulary during lessons. |
| `user.preferences.lessons_batch_size` | body | `number` | no | Number of subjects introduced during lessons before quizzing. |
| `user.preferences.reviews_autoplay_audio` | body | `boolean` | no | Automatically play pronunciation audio for vocabulary during reviews. |
| `user.preferences.reviews_display_srs_indicator` | body | `boolean` | no | Display the SRS change indicator after a subject is completely answered during review. |
| `user.preferences.reviews_presentation_order` | body | `string` | no | The order in which reviews are presented. |
