# Feeder Privacy Policy

Last updated: 20 September 2026

Feeder is developed by **YooooEX**. This policy describes data handling in the current multiplatform Feeder application for Android, iOS, and desktop. Older releases may behave differently. For privacy questions or requests, contact **me@yooooex.com**.

## Reader services and reading activity

Feeder is a client for the Reader service you choose or configure, such as a self-hosted FreshRSS service. It does not create a separate Feeder account. To sign in and provide reading features, Feeder sends authentication information to that service and exchanges subscription, folder, article, and account information with it.

Depending on the login method, authentication information includes your username and password or an authorization token. Reader requests also include the information needed for the action: feed addresses when subscribing, article or feed identifiers, read and starred status changes, and synchronization or pagination parameters. These exchanges let you retrieve articles, manage subscriptions, and synchronize reading activity. Your Reader service controls its own account records, server logs, storage, and deletion processes.

## Images, links, sharing, and proxies

Displaying articles, thumbnails, and feed icons can make requests to the servers hosting those images. Those servers receive the requested address and network connection information, such as your IP address. They are not necessarily the same server as your Reader service.

Opening an original article or a link passes its address to your browser or the system's associated application. Sharing can pass an article's title and link to the system sharing interface and the application you select. On desktop, sharing copies the link to your clipboard; some mobile fallback paths also copy a link. These applications, websites, and clipboard services handle the information according to their own settings and policies.

If you configure a proxy, it may carry supported Reader or AI connections and receive connection information. The proxy setting does not cover every network request made by Feeder or by an external application, and using a proxy does not by itself encrypt a connection.

## Optional AI features

AI features are off by default. When you configure and use them, requests go to the AI service endpoint you provide. That service receives your API token for authentication, the selected model, and the messages needed for the requested feature.

- **Summaries:** after you enable AI and automatic summaries, opening or switching articles can automatically send the article title, source URL, extracted article text, and target language to the configured service.
- **Translation:** requesting a translation sends the corresponding article information and target language. Enabling the translation option alone does not automatically translate articles.
- **Connection testing:** pressing Test sends your API token, model, and fixed test instructions asking for an “OK” response. It does not send article content.

For summaries and translations, Feeder sends up to 12,000 characters of extracted text from the available article content. This limit does not include the title, source URL, or other request fields. Successful results may be reused during the current session; retrying can send another request.

The AI service's storage and use of the information, including any use for model training, are governed by that service's policies and your agreement or settings with it. Feeder cannot apply one retention period or training policy to every endpoint. Disabling a feature or cancelling a request does not withdraw information the service has already received.

## Usage and crash diagnostics on Android

The Android application uses Google Firebase Analytics and Crashlytics for optional usage measurement and crash diagnosis. The combined usage and crash diagnostics setting is **off by default**. Enabling it saves your choice for the next application startup.

When enabled, Feeder's own usage events report the login method and whether login succeeded, and that a share action occurred. These event parameters do not include your article title, article identifier, source URL, account details, or tokens.

Firebase also processes technical information for these services. Depending on the SDK, configuration, and collection state, this includes application-instance or installation identifiers, app and device metadata, session and interaction information, crash stack traces and app state, and approximate location derived from IP information. Analytics can also process advertising-related identifiers where available and allowed by configuration. These automatic SDK data are separate from Feeder's limited event parameters. Firebase Installations and Sessions support the diagnostic services. Google processes the information, and the developer can access analytics and diagnostic reports through Firebase and Google Analytics.

Turning the setting off immediately stops Feeder's own usage events and requests that both SDKs disable collection. Feeder also requests a local Analytics reset and deletion of eligible unsent crash reports. These are not a guarantee of immediate or complete deletion: SDK initialization can still occur, startup state may take subsequent launches to settle, and work already in progress or queued data may still be processed or sent. Turning the setting back on does not reopen collection during that same application process. These controls do not recall information already uploaded to Google.

The current iOS and desktop applications do not use this Firebase telemetry integration. For information about Google's processing, see [Firebase privacy information](https://firebase.google.com/support/privacy) and [Google's Privacy Policy](https://policies.google.com/privacy).

## Information stored on your device

Feeder stores Reader authentication and account information, server settings, AI endpoint/token/model settings, proxy settings, and other preferences locally so they remain available when you reopen the application. These preferences use the application's normal local storage; Feeder does not add a separate encryption layer for stored tokens. Operating-system access controls and any device encryption still depend on your platform and settings.

Images can be cached on disk and in memory. Article, subscription, and AI-result state is also kept in memory while the application runs. Operating-system backup and restore features may retain or restore local application data according to their own settings.

Feeder's HTTP logging configuration disables full request/response logging in release builds. Development builds can log request and response bodies, and local application logs can contain operational information; for example, desktop sharing writes the shared URL to local output. Local logs are distinct from the limited Firebase event parameters described above.

## Transmission security

AI requests require HTTPS on Android and iOS, including requests to local-network endpoints. Desktop AI endpoints can use HTTP or HTTPS. Reader endpoints can be configured with HTTP or HTTPS; platform security restrictions may prevent some connections, particularly on iOS. Images, external websites, browsers, and proxy connections have their own transport behavior.

Consequently, not all connections supported by Feeder are guaranteed to be encrypted. HTTP connections can expose credentials and content to parties on the network. Use trusted services and HTTPS endpoints where available. Google documents HTTPS transport for the Firebase data described above; this does not extend to every other service you configure.

## Retention, deletion, and your choices

- **Local data:** settings and credentials remain until changed or the relevant local data are removed. Logging out clears the Reader identity and active Reader/AI session state, but retains AI configuration and tokens, proxy settings, other preferences, and disk image caches. Clear Cache removes Feeder's managed disk cache, not credentials, all in-memory state, backups, or remote data. Use your operating system's application-data controls for further local cleanup. On desktop, removing the application package alone may leave its data in `~/.feeder`; you can remove that directory after closing Feeder. Backups must be managed through the relevant backup service.
- **Reader services:** logging out does not delete your Reader account or its subscriptions and history. Use your Reader service's account and deletion controls or contact that provider. Its retention rules govern data stored there.
- **AI services:** you can disable the AI features or change their configuration. Deletion of previously submitted data must be handled through the AI service, subject to its policy and your account settings. Feeder does not provide a remote deletion command for arbitrary AI endpoints.
- **Firebase:** the Android setting controls the collection requests described above. Previously uploaded information remains subject to the applicable Google/Firebase retention processes and project settings; local reset and unsent-report deletion do not erase it. [Firebase's published policy](https://firebase.google.com/support/privacy) states that Crashlytics retains crash stack traces and associated installation identifiers for 90 days before beginning removal from live and backup systems; this is not a guarantee that all copies disappear on day 90. Analytics retention depends on the applicable service and project settings. Contact **me@yooooex.com** about developer-managed analytics or diagnostic data and available deletion options.

You may also contact **me@yooooex.com** with questions about this policy or requests concerning information under the developer's control. Do not send passwords or API tokens with a request. Requests concerning accounts or data held by your chosen Reader or AI service should be directed to that service.

## Changes to this policy

This policy may be updated as Feeder's features or data handling change. The public policy linked from the application will contain the updated text. Platform-specific statements refer to the current multiplatform application and should not be assumed to describe every historical release.
