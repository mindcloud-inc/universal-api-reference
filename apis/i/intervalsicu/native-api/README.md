# Intervals.icu: Native API Reference

A consolidated summary of Intervals.icu's API configuration and 144 documented operations, with links to official documentation.

- **Official docs:** https://intervals.icu/api/v1/docs
- **OpenAPI specification:** https://intervals.icu/api/v1/docs
- **API base URL:** `https://intervals.icu`

## Authentication

### Basic API Key

Use Intervals.icu personal API key authentication over HTTP Basic. The username must be the literal string API_KEY and the password is your personal Intervals.icu API key from Settings.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://intervals.icu/api/v1/docs)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 3 after each failed attempt.

## Endpoints (144 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Activity Message](actions/add-activity-message.md) | `POST /api/v1/activity/:id/messages` | [docs](https://intervals.icu/api/v1/docs) |
| [Apply Event Plan](actions/apply-event-plan.md) | `POST /api/v1/athlete/:id/events/apply-plan` | [docs](https://intervals.icu/api/v1/docs) |
| [Apply Plan Changes](actions/apply-plan-changes.md) | `PUT /api/v1/athlete/:id/apply-plan-changes` | [docs](https://intervals.icu/api/v1/docs) |
| [Apply Sport Settings](actions/apply-sport-settings.md) | `PUT /api/v1/athlete/:athleteId/sport-settings/:id/apply` | [docs](https://intervals.icu/api/v1/docs) |
| [Bulk Delete Events](actions/bulk-delete-events.md) | `PUT /api/v1/athlete/:id/events/bulk-delete` | [docs](https://intervals.icu/api/v1/docs) |
| [Compare Route Similarity](actions/compare-route-similarity.md) | `GET /api/v1/athlete/:id/routes/:route_id/similarity/:other_id` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Activities from File](actions/create-activities-from-file.md) | `POST /api/v1/athlete/:id/activities` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Custom Item](actions/create-custom-item.md) | `POST /api/v1/athlete/:id/custom-item` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Event](actions/create-event.md) | `POST /api/v1/athlete/:id/events` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Events](actions/create-events.md) | `POST /api/v1/athlete/:id/events/bulk` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Folder](actions/create-folder.md) | `POST /api/v1/athlete/:id/folders` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Gear](actions/create-gear.md) | `POST /api/v1/athlete/:id/gear` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Gear Reminder](actions/create-gear-reminder.md) | `POST /api/v1/athlete/:id/gear/:gearId/reminder` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Manual Activities](actions/create-manual-activities.md) | `POST /api/v1/athlete/:id/activities/manual/bulk` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Manual Activity](actions/create-manual-activity.md) | `POST /api/v1/athlete/:id/activities/manual` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Sport Settings](actions/create-sport-settings.md) | `POST /api/v1/athlete/:athleteId/sport-settings` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Workout](actions/create-workout.md) | `POST /api/v1/athlete/:id/workouts` | [docs](https://intervals.icu/api/v1/docs) |
| [Create Workouts](actions/create-workouts.md) | `POST /api/v1/athlete/:id/workouts/bulk` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Activity](actions/delete-activity.md) | `DELETE /api/v1/activity/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Chat Message](actions/delete-chat-message.md) | `DELETE /api/v1/chats/:id/messages/:msgId` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Custom Item](actions/delete-custom-item.md) | `DELETE /api/v1/athlete/:id/custom-item/:itemId` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Event](actions/delete-event.md) | `DELETE /api/v1/athlete/:id/events/:eventId` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Events in Range](actions/delete-events-in-range.md) | `DELETE /api/v1/athlete/:id/events` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /api/v1/athlete/:id/folders/:folderId` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Gear](actions/delete-gear.md) | `DELETE /api/v1/athlete/:id/gear/:gearId` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Gear Reminder](actions/delete-gear-reminder.md) | `DELETE /api/v1/athlete/:id/gear/:gearId/reminder/:reminderId` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Intervals](actions/delete-intervals.md) | `PUT /api/v1/activity/:id/delete-intervals` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Sport Settings](actions/delete-sport-settings.md) | `DELETE /api/v1/athlete/:athleteId/sport-settings/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Delete Workout](actions/delete-workout.md) | `DELETE /api/v1/athlete/:id/workouts/:workoutId` | [docs](https://intervals.icu/api/v1/docs) |
| [Disconnect App](actions/disconnect-app.md) | `DELETE /api/v1/disconnect-app` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Activities CSV](actions/download-activities-csv.md) | `GET /api/v1/athlete/:id/activities.csv` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Activity File](actions/download-activity-file.md) | `GET /api/v1/activity/:id/file` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Activity FIT File](actions/download-activity-fit-file.md) | `GET /api/v1/activity/:id/fit-file` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Activity FIT Files](actions/download-activity-fit-files.md) | `POST /api/v1/athlete/:id/download-fit-files` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Activity GPX File](actions/download-activity-gpx-file.md) | `GET /api/v1/activity/:id/gpx-file` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Event Workout](actions/download-event-workout.md) | `GET /api/v1/athlete/:id/events/:eventId/download:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Workout](actions/download-workout.md) | `POST /api/v1/athlete/:id/download-workout:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Workout File](actions/download-workout-file.md) | `POST /api/v1/download-workout:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Download Workouts ZIP](actions/download-workouts-zip.md) | `GET /api/v1/athlete/:id/workouts.zip` | [docs](https://intervals.icu/api/v1/docs) |
| [Duplicate Events](actions/duplicate-events.md) | `POST /api/v1/athlete/:id/duplicate-events` | [docs](https://intervals.icu/api/v1/docs) |
| [Duplicate Workouts](actions/duplicate-workouts.md) | `POST /api/v1/athlete/:id/duplicate-workouts` | [docs](https://intervals.icu/api/v1/docs) |
| [Find Activities by Intervals](actions/find-activities-by-intervals.md) | `GET /api/v1/athlete/:id/activities/interval-search` | [docs](https://intervals.icu/api/v1/docs) |
| [Find Best Efforts](actions/find-best-efforts.md) | `GET /api/v1/activity/:id/best-efforts` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity](actions/get-activity.md) | `GET /api/v1/activity/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Heart Rate Curve](actions/get-activity-heart-rate-curve.md) | `GET /api/v1/activity/:id/hr-curve:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Heart Rate Curves](actions/get-activity-heart-rate-curves.md) | `GET /api/v1/athlete/:id/activity-hr-curves:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Intervals](actions/get-activity-intervals.md) | `GET /api/v1/activity/:id/intervals` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Map](actions/get-activity-map.md) | `GET /api/v1/activity/:id/map` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Pace Curve](actions/get-activity-pace-curve.md) | `GET /api/v1/activity/:id/pace-curve:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Pace Curves](actions/get-activity-pace-curves.md) | `GET /api/v1/athlete/:id/activity-pace-curves:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Power Curve](actions/get-activity-power-curve.md) | `GET /api/v1/activity/:id/power-curve:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Power Curves](actions/get-activity-power-curves.md) | `GET /api/v1/athlete/:id/activity-power-curves:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Power Spike Model](actions/get-activity-power-spike-model.md) | `GET /api/v1/activity/:id/power-spike-model` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Segments](actions/get-activity-segments.md) | `GET /api/v1/activity/:id/segments` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Streams](actions/get-activity-streams.md) | `GET /api/v1/activity/:id/streams:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Activity Weather Summary](actions/get-activity-weather-summary.md) | `GET /api/v1/activity/:id/weather-summary` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Athlete](actions/get-athlete.md) | `GET /api/v1/athlete/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Athlete Power vs Heart Rate Curve](actions/get-athlete-power-vs-heart-rate-curve.md) | `GET /api/v1/athlete/:id/power-hr-curve` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Athlete Profile](actions/get-athlete-profile.md) | `GET /api/v1/athlete/:id/profile` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Athlete Settings](actions/get-athlete-settings.md) | `GET /api/v1/athlete/:id/settings/:deviceClass` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Athlete Summary](actions/get-athlete-summary.md) | `GET /api/v1/athlete/:id/athlete-summary:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Chat](actions/get-chat.md) | `GET /api/v1/chats/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Custom Item](actions/get-custom-item.md) | `GET /api/v1/athlete/:id/custom-item/:itemId` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Event](actions/get-event.md) | `GET /api/v1/athlete/:id/events/:eventId` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Gap Histogram](actions/get-gap-histogram.md) | `GET /api/v1/activity/:id/gap-histogram` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Heart Rate Histogram](actions/get-heart-rate-histogram.md) | `GET /api/v1/activity/:id/hr-histogram` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Heart Rate Training Load Model](actions/get-heart-rate-training-load-model.md) | `GET /api/v1/activity/:id/hr-load-model` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Interval Stats](actions/get-interval-stats.md) | `GET /api/v1/activity/:id/interval-stats` | [docs](https://intervals.icu/api/v1/docs) |
| [Get MMP Model](actions/get-mmp-model.md) | `GET /api/v1/athlete/:id/mmp-model` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Multiple Activities](actions/get-multiple-activities.md) | `GET /api/v1/athlete/:athleteId/activities/:ids` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Pace Histogram](actions/get-pace-histogram.md) | `GET /api/v1/activity/:id/pace-histogram` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Power Histogram](actions/get-power-histogram.md) | `GET /api/v1/activity/:id/power-histogram` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Power vs Heart Rate](actions/get-power-vs-heart-rate.md) | `GET /api/v1/activity/:id/power-vs-hr:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Route](actions/get-route.md) | `GET /api/v1/athlete/:id/routes/:route_id` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Shared Event](actions/get-shared-event.md) | `GET /api/v1/shared-event/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Sport Settings](actions/get-sport-settings.md) | `GET /api/v1/athlete/:athleteId/sport-settings/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Time at Heart Rate](actions/get-time-at-heart-rate.md) | `GET /api/v1/activity/:id/time-at-hr` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Training Plan](actions/get-training-plan.md) | `GET /api/v1/athlete/:id/training-plan` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Weather Configuration](actions/get-weather-configuration.md) | `GET /api/v1/athlete/:id/weather-config` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Weather Forecast](actions/get-weather-forecast.md) | `GET /api/v1/athlete/:id/weather-forecast` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Wellness Record](actions/get-wellness-record.md) | `GET /api/v1/athlete/:id/wellness/:date` | [docs](https://intervals.icu/api/v1/docs) |
| [Get Workout](actions/get-workout.md) | `GET /api/v1/athlete/:id/workouts/:workoutId` | [docs](https://intervals.icu/api/v1/docs) |
| [Import Workout](actions/import-workout.md) | `POST /api/v1/athlete/:id/folders/:folderId/import-workout` | [docs](https://intervals.icu/api/v1/docs) |
| [List Activities](actions/list-activities.md) | `GET /api/v1/athlete/:id/activities` | [docs](https://intervals.icu/api/v1/docs) |
| [List Activity Messages](actions/list-activity-messages.md) | `GET /api/v1/activity/:id/messages` | [docs](https://intervals.icu/api/v1/docs) |
| [List Activity Power Curves](actions/list-activity-power-curves.md) | `GET /api/v1/activity/:id/power-curves:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [List Activity Tags](actions/list-activity-tags.md) | `GET /api/v1/athlete/:id/activity-tags` | [docs](https://intervals.icu/api/v1/docs) |
| [List Athlete Chats](actions/list-athlete-chats.md) | `GET /api/v1/athlete/:id/chats` | [docs](https://intervals.icu/api/v1/docs) |
| [List Athlete Gear](actions/list-athlete-gear.md) | `GET /api/v1/athlete/:id/gear:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /api/v1/chats/:id/messages` | [docs](https://intervals.icu/api/v1/docs) |
| [List Custom Items](actions/list-custom-items.md) | `GET /api/v1/athlete/:id/custom-item` | [docs](https://intervals.icu/api/v1/docs) |
| [List Event Tags](actions/list-event-tags.md) | `GET /api/v1/athlete/:id/event-tags` | [docs](https://intervals.icu/api/v1/docs) |
| [List Events](actions/list-events.md) | `GET /api/v1/athlete/:id/events:format` | [docs](https://intervals.icu/api/v1/docs) |
| [List Fitness Model Events](actions/list-fitness-model-events.md) | `GET /api/v1/athlete/:id/fitness-model-events` | [docs](https://intervals.icu/api/v1/docs) |
| [List Folders](actions/list-folders.md) | `GET /api/v1/athlete/:id/folders` | [docs](https://intervals.icu/api/v1/docs) |
| [List Global Pace Distances](actions/list-global-pace-distances.md) | `GET /api/v1/pace_distances` | [docs](https://intervals.icu/api/v1/docs) |
| [List Heart Rate Curves](actions/list-heart-rate-curves.md) | `GET /api/v1/athlete/:id/hr-curves:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [List Matching Activities](actions/list-matching-activities.md) | `GET /api/v1/athlete/:athleteId/sport-settings/:id/matching-activities` | [docs](https://intervals.icu/api/v1/docs) |
| [List Nearby Activities](actions/list-nearby-activities.md) | `GET /api/v1/athlete/:id/activities-around` | [docs](https://intervals.icu/api/v1/docs) |
| [List Pace Curves](actions/list-pace-curves.md) | `GET /api/v1/athlete/:id/pace-curves:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [List Pace Distances](actions/list-pace-distances.md) | `GET /api/v1/athlete/:athleteId/sport-settings/:id/pace_distances` | [docs](https://intervals.icu/api/v1/docs) |
| [List Power Curves](actions/list-power-curves.md) | `GET /api/v1/athlete/:id/power-curves:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [List Routes](actions/list-routes.md) | `GET /api/v1/athlete/:id/routes` | [docs](https://intervals.icu/api/v1/docs) |
| [List Shared Folder Athletes](actions/list-shared-folder-athletes.md) | `GET /api/v1/athlete/:id/folders/:folderId/shared-with` | [docs](https://intervals.icu/api/v1/docs) |
| [List Sport Settings](actions/list-sport-settings.md) | `GET /api/v1/athlete/:athleteId/sport-settings` | [docs](https://intervals.icu/api/v1/docs) |
| [List Wellness Records](actions/list-wellness-records.md) | `GET /api/v1/athlete/:id/wellness:ext` | [docs](https://intervals.icu/api/v1/docs) |
| [List Workout Tags](actions/list-workout-tags.md) | `GET /api/v1/athlete/:id/workout-tags` | [docs](https://intervals.icu/api/v1/docs) |
| [List Workouts](actions/list-workouts.md) | `GET /api/v1/athlete/:id/workouts` | [docs](https://intervals.icu/api/v1/docs) |
| [Mark Event Done](actions/mark-event-done.md) | `POST /api/v1/athlete/:id/events/:eventId/mark-done` | [docs](https://intervals.icu/api/v1/docs) |
| [Recalculate Gear Stats](actions/recalculate-gear-stats.md) | `GET /api/v1/athlete/:id/gear/:gearId/calc` | [docs](https://intervals.icu/api/v1/docs) |
| [Reorder Custom Items](actions/reorder-custom-items.md) | `PUT /api/v1/athlete/:id/custom-item-indexes` | [docs](https://intervals.icu/api/v1/docs) |
| [Replace Gear](actions/replace-gear.md) | `POST /api/v1/athlete/:id/gear/:gearId/replace` | [docs](https://intervals.icu/api/v1/docs) |
| [Search Activities](actions/search-activities.md) | `GET /api/v1/athlete/:id/activities/search` | [docs](https://intervals.icu/api/v1/docs) |
| [Search Full Activities](actions/search-full-activities.md) | `GET /api/v1/athlete/:id/activities/search-full` | [docs](https://intervals.icu/api/v1/docs) |
| [Send Message](actions/send-message.md) | `POST /api/v1/chats/send-message` | [docs](https://intervals.icu/api/v1/docs) |
| [Split Interval](actions/split-interval.md) | `PUT /api/v1/activity/:id/split-interval` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Activity](actions/update-activity.md) | `PUT /api/v1/activity/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Activity Streams](actions/update-activity-streams.md) | `PUT /api/v1/activity/:id/streams` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Athlete](actions/update-athlete.md) | `PUT /api/v1/athlete/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Athlete Plans](actions/update-athlete-plans.md) | `PUT /api/v1/athlete-plans` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Chat Message](actions/update-chat-message.md) | `PUT /api/v1/chats/:id/messages/:msgId` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Custom Item](actions/update-custom-item.md) | `PUT /api/v1/athlete/:id/custom-item/:itemId` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Event](actions/update-event.md) | `PUT /api/v1/athlete/:id/events/:eventId` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Events](actions/update-events.md) | `PUT /api/v1/athlete/:id/events` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Folder](actions/update-folder.md) | `PUT /api/v1/athlete/:id/folders/:folderId` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Folder Sharing](actions/update-folder-sharing.md) | `PUT /api/v1/athlete/:id/folders/:folderId/shared-with` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Gear](actions/update-gear.md) | `PUT /api/v1/athlete/:id/gear/:gearId` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Gear Reminder](actions/update-gear-reminder.md) | `PUT /api/v1/athlete/:id/gear/:gearId/reminder/:reminderId` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Interval](actions/update-interval.md) | `PUT /api/v1/activity/:id/intervals/:intervalId` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Intervals](actions/update-intervals.md) | `PUT /api/v1/activity/:id/intervals` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Last Seen Message](actions/update-last-seen-message.md) | `PUT /api/v1/chats/:id/messages/:msgId/seen` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Multiple Sport Settings](actions/update-multiple-sport-settings.md) | `PUT /api/v1/athlete/:athleteId/sport-settings` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Plan Workouts](actions/update-plan-workouts.md) | `PUT /api/v1/athlete/:id/folders/:folderId/workouts` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Route](actions/update-route.md) | `PUT /api/v1/athlete/:id/routes/:route_id` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Sport Settings](actions/update-sport-settings.md) | `PUT /api/v1/athlete/:athleteId/sport-settings/:id` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Training Plan](actions/update-training-plan.md) | `PUT /api/v1/athlete/:id/training-plan` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Weather Configuration](actions/update-weather-configuration.md) | `PUT /api/v1/athlete/:id/weather-config` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Wellness Record](actions/update-wellness-record.md) | `PUT /api/v1/athlete/:id/wellness` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Wellness Record by Date](actions/update-wellness-record-by-date.md) | `PUT /api/v1/athlete/:id/wellness/:date` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Wellness Records Bulk](actions/update-wellness-records-bulk.md) | `PUT /api/v1/athlete/:id/wellness-bulk` | [docs](https://intervals.icu/api/v1/docs) |
| [Update Workout](actions/update-workout.md) | `PUT /api/v1/athlete/:id/workouts/:workoutId` | [docs](https://intervals.icu/api/v1/docs) |
| [Upload Activity Streams CSV](actions/upload-activity-streams-csv.md) | `PUT /api/v1/activity/:id/streams.csv` | [docs](https://intervals.icu/api/v1/docs) |
| [Upload Custom Item Image](actions/upload-custom-item-image.md) | `POST /api/v1/athlete/:id/custom-item/:itemId/image` | [docs](https://intervals.icu/api/v1/docs) |
| [Upload Wellness Records](actions/upload-wellness-records.md) | `POST /api/v1/athlete/:id/wellness` | [docs](https://intervals.icu/api/v1/docs) |
