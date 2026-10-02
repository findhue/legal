---
title: Privacy Policy
description: FindHue's Privacy Policy — what we collect, why, and who else can see it.
slug: privacy
updated: October 2, 2026
---

## Who we are

FindHue is operated by **EduMon Studios LLC** ("EduMon Studios," "we," "us," or "our"). If you have
questions about this policy or your data, see [Contact](#contact) below.

## The short version

FindHue is a color-matching photo game you play solo, with Friend Groups, and in timed Parties.
Photos from private capture attempts stay on your device unless you deliberately publish one as a
Daily Find or Party Find, but the app and its service providers also process account, connection,
security, diagnostic, analytics, and advertising information needed to operate the service. We
don't sell your data. The sections below explain what's collected, why, and who else may process
it.

## Information you provide directly

- **Display name and avatar.** You can set a display name (shown to friends) and a profile
  picture. Your avatar photo stays on your device only — it is never uploaded anywhere. Your
  display name is stored on our server (Supabase) so friends can see who's who.
- **Sign in with Apple.** FindHue works from the moment you open it, with no login screen. FindHue
  automatically creates an anonymous account identity so backend features such as publishing,
  Friends, Friend Groups, Parties, reports, and account ownership can work without requiring you to
  sign in first. If you choose **Settings → Save account with Apple**, FindHue uses Sign in with
  Apple to attach a permanent identity to that same anonymous account, without replacing its
  existing server-side data. Depending on what you allow Apple to share, this can include your name
  and an email address (which may be an Apple-generated private relay address rather than your real
  one). We store Apple's own stable, per-app identifier for your account for reference; we do not
  use it for anything beyond making sign-in work.
- **Friend connections.** Adding a friend (by invite code or QR scan), accepting or declining a
  friend request, and removing or blocking someone are all stored against your account so the
  Friends feature works.
- **Friend Groups.** Creating, joining, or leaving a Friend Group, and your membership/role in it,
  are stored the same way.
- **Parties.** Creating, joining, leaving, or being removed from a Group Party or Quick Party, and
  your participation and results in it, are stored against your account while that Party's own data
  exists (see [Retention](#retention)).
- **Reports.** If you report another user's Daily Find or Party Find, we store who filed the
  report, who/what was reported, the reason you selected, and any note you added. Reports are
  visible only to FindHue for review — never to other users, including the person you reported.

## Daily Finds and Party Finds

- **Every private capture attempt is saved locally**, whether or not you ever publish it — this
  applies to the daily challenge and to every Party. Taking or scoring a photo does not itself
  upload it. Local history may include the photo, challenge date, score, target and found colors,
  selected point, and related local metadata. FindHue does not cloud-sync this entire history.
- **Publishing a Daily Find** is a separate, deliberate action ("Make This My Find"). Only photos
  you deliberately choose to publish as your Daily Find, including any later Find replacements, are
  uploaded to our storage provider (Cloudflare R2) and sent through moderation. Your other private
  capture attempts remain on your device. Only one active Daily Find is visible for a challenge day
  at a time.
- **Submitting a Party Find** is also a separate, deliberate action, available only while a Party
  you joined is live. Only the photo you choose to submit to that Party is uploaded and sent through
  moderation; it is visible to other participants in that same Party only once the Party's countdown
  ends and results are revealed.
- Photos are re-encoded before upload, which removes normal embedded EXIF/GPS and device metadata
  from the uploaded image. FindHue does not request precise iOS location permission for the daily
  challenge or for Parties, and does not intentionally upload GPS coordinates from Find photos.
  Third parties such as Google may infer coarse location from network or IP information.
- Your device never receives a permanent public link to an uploaded photo — only short-lived,
  expiring download links generated on demand by our server, and only for people who are actually
  allowed to see that photo (you, or eligible friends, Friend Group members, or Party participants
  after moderation approval).
- **Published Daily Find photos are scheduled for automatic deletion approximately 72 hours after
  publishing.** **Party Find photos become inaccessible once that Party's 24-hour results window
  ends, and the underlying file is then deleted from cloud storage.** In both cases, operational
  failures, retries, legal or security needs, or similar circumstances may occasionally cause
  physical deletion to occur somewhat later than scheduled. Score, date, color, and similar metadata
  may be retained longer as part of your personal History (see [Retention](#retention)).

## The 7 PM Pacific social cutoff and Late Finds

Each day's challenge resets at midnight Pacific Time. A Daily Find can be newly published or
replaced only before **7 PM Pacific Time** that same day. After 7 PM Pacific and before the next
midnight-Pacific rollover, you can still complete a Find for that day for your own private History
and Collection progress — a "Late Find" — but it cannot be newly published socially, and it cannot
replace or delete a Daily Find you already published before the cutoff. A Late Find's photo is
never uploaded to our servers; it stays on your device like any other capture attempt. This cutoff
is specific to the Daily challenge — a Party simply ends at its own scheduled time, after which no
further submissions to that Party are possible.

## Automated content moderation

Every newly published Daily Find and every submitted Party Find is screened by Microsoft Azure AI
Content Safety before it is shown to anyone else. FindHue sends the image needed for moderation;
profile or social information is not intentionally included in that image request. Moderation
failures fail closed: a transient failure or unrecognized result holds the Find back rather than
approving it automatically. We may retain the verdict, category, severity, provider, policy, and
timestamp for moderation and safety operations. Automated moderation is not infallible.

## Friends, groups, and Party reactions

Your published Daily Find can be shown to accepted friends and eligible Friend Group members after
moderation approval, and only for a short window: the current and immediately prior challenge. The
photo may be visible before the daily reveal; scores, reaction totals, and reveal results remain
hidden until that challenge's 7 PM Pacific reveal time. A Party Find can be shown to other
participants in that same Party after moderation approval, with scores and results hidden until
that Party's own reveal when the countdown ends. FindHue does not keep a scrollable public history
of old posts. Hearts are tied internally to an account for enforcement but anonymous to other users.
FindHue may calculate Closest Match and Crowd Favorite for the daily challenge, and an equivalent
winner/closest-match result for a Party; these are entertainment and social features, not financial
prizes.

## Automatically collected technical data

Backend infrastructure and SDKs may process technical information such as IP address, operating
system, device and platform data, app version and build, request timestamps, network/server logs,
internal account identifiers, crash data, stack traces, performance data, advertising interactions,
and related ad-delivery information.

## How we use information and legal bases

FindHue uses information for account and authentication, publishing Daily Finds and Party Finds,
Friends, Friend Groups, Parties, moderation, reporting and blocking, reactions and reveals, push and
local reminder notifications, anti-abuse limits, rewarded ads, diagnostics, analytics, security and
fraud prevention, and legal obligations. Depending on the situation, our legal basis may be
performance of the service contract, legitimate interests, consent, or legal obligations. Consent is
not the legal basis for every processing activity.

## Privacy rights

Depending on where you live, you may have rights to access, correct, delete, restrict or object to
processing, receive portable data, withdraw consent, and complain to a data-protection authority. We
may need to verify your identity before completing a request. Contact us using the details below.

## Notifications

FindHue offers two separate kinds of notification, and you control each independently in **Settings
→ Notifications**:

- **Morning and Evening reminders** are generated entirely on your device — they work even offline,
  and always show that day's real color. They never require a server round-trip and are not
  "push notifications" in the sense below.
- **Push notifications** — **Group Party Created**, **Party Started**, and **Daily Reveal Ready** —
  are delivered to your device by a push service. If you grant notification permission, FindHue
  registers your device for push delivery through Expo's push notification service, which in turn
  relies on Apple's push infrastructure (APNs) on iOS and equivalent platform push infrastructure on
  Android. This registration (an opaque device push token, tied to your account so we know where to
  deliver a notification) is used only to deliver the specific notification types you've enabled; it
  is not used for advertising or analytics.

## Analytics and crash diagnostics

FindHue uses PostHog for basic product analytics and crash/error reporting, active only in
production/TestFlight builds (never during local development). What this does and doesn't include:

- You're identified to PostHog only by an opaque internal account identifier — never your name,
  email, avatar, or any other personal detail.
- Every event FindHue sends goes through an allow-listed vocabulary of specific product events
  (e.g., "a Find was published," "a Party was started," "a rewarded ad was watched") — not a general
  activity log.
- A defense-in-depth filter strips anything that looks like a token, password, email address,
  photo/file URI, invite code, or similar sensitive value from every event and crash report before
  it's sent, even if it were accidentally included.
- Session replay, precise location/GeoIP enrichment, surveys, and remote feature flags are all
  turned off — FindHue doesn't use any of them.
- Crash reports may include technical diagnostic information (device/OS type, app version, stack
  traces) needed to fix bugs.

## Advertising

The first 3 Find submissions or replacements per challenge day are free — this allowance is shared
across your Daily Find and every Party you play that same day, not a separate allowance per Party.
After that allowance is used, an additional Find submission (Daily or Party) may require one
successfully completed and server-verified rewarded ad. Private captures and scoring remain
unlimited and do not require an ad. FindHue requests non-personalized ads, does not request App
Tracking Transparency permission, and does not intentionally provide Google with your Find photo,
display name, email, friend list, or private history. Google and ad infrastructure may nevertheless
process IP address, coarse location inferred from IP, device and app identifiers, ad interactions,
advertising and consent data, crash/performance information, and related ad-delivery data.
Rewarded-ad completion is granted only after server-side verification.

_Note: AdMob and Google's underlying ad-serving infrastructure are third-party services we don't
fully control — see [Third-party services](#third-party) below._

## Third-party services {#third-party}

FindHue relies on service providers and third-party services to operate the app. Each may process
the categories described below under its own terms and privacy practices. We require service
providers that process FindHue user data on our behalf to use it only for the purposes for which it
was provided and to provide protections consistent with this Privacy Policy, applicable law, and
applicable platform requirements.

| Service | What it's used for | What it can see |
|---|---|---|
| **Apple** | Sign-in, App Store distribution, and push-notification delivery (via Expo's push service) for Group Party Created, Party Started, and Daily Reveal Ready | Whatever you choose to share via Sign in with Apple; an opaque device push token for delivering enabled push notifications |
| **Supabase** | Our backend database and authentication | Your account, profile, friend graph, groups, Party data, reports, and Find metadata |
| **Cloudflare R2** | Temporary storage for published Daily Find and submitted Party Find photos | The selected photo, scheduled for deletion on the schedule described in [Daily Finds and Party Finds](#daily-finds-and-party-finds) |
| **Microsoft Azure AI Content Safety** | Automated photo moderation for Daily Finds and Party Finds | The photo file only, at the moment you publish or submit it |
| **PostHog** | Analytics and crash reporting | An opaque account identifier and sanitized event/crash data |
| **Google AdMob** | Optional rewarded video ads and consent management | Ad-request, device/app, IP/coarse-location, consent, interaction, crash, and performance data |

Each provider also maintains its own privacy practices and security logs. We do not control
independent aspects of a provider's business; see its privacy policy for details about how it
handles data on its side.

## Retention and deletion {#retention}

- **Local device data** (your private capture history, avatar, app settings, reminder times) stays
  on your device until you clear it or uninstall the app.
- **Published Daily Find photos** are scheduled for deletion approximately 72 hours after
  publishing. **Party Find photos** become inaccessible once that Party's 24-hour results window
  ends and are then deleted from cloud storage. In both cases operational failures, retries,
  legal/security needs, or similar circumstances may delay physical deletion. Metadata may remain
  longer.
- **Find metadata** (score, date, target/found color, whether and where it was published) is kept
  as part of your personal History for as long as your account exists.
- **Reports, blocks, and moderation records** are kept for as long as your account exists, to keep
  the reporting/blocking system working correctly.
- **Deleting your account** (Settings → Delete account) permanently removes the server-side
  account/auth identity and associated social, Party, and account data. See
  [Account deletion](#account-deletion) below for exactly what this does.

## Account deletion {#account-deletion}

Settings → Delete account is available to anyone using the app — you don't need to have saved your
account with Sign in with Apple first. It:

1. Deletes your profile and, through it, every friendship, friend request, group membership, Party
   participation, report, block, reaction, and Find record tied to your account.
2. Deletes the underlying account identity itself (not just the data associated with it), so nothing
   about you remains sign-in-able afterward.

This can't be undone. Cloud-object deletion may finish asynchronously. Deleting your account is
separate from **Settings → Clear all records**, which erases local-only private captures from that
device; uninstalling the app also handles local-only data. Delete account does not necessarily
synchronously erase every local file.

## Local device data

Your private capture history (every Daily and Party Find attempt, published or not), your avatar
photo, your app preferences, and your reminder settings are stored only on your device using
standard iOS local storage. FindHue never uploads this local history. Only photos you deliberately
choose to publish as a Daily Find (including later replacements) or submit to a live Party are
uploaded; your other private attempts remain on your device.

## Security

Data in transit to and from Supabase, Cloudflare R2, and Azure is encrypted (HTTPS/TLS). Access to
your data on our backend is enforced by database-level row-level-security rules scoped to your own
account. Photo storage uses short-lived, single-purpose links rather than permanent public URLs. No
system is perfectly secure, and we can't guarantee absolute security of any information you transmit
to us.

## International data processing

FindHue's backend and analytics infrastructure run on servers operated by our service providers,
which may be located in the United States or other countries. By using FindHue, you understand your
information may be processed outside your own country.

## Children

FindHue is a general-audience service and is not directed to children under 13. You must be at
least 13 and old enough under the laws where you live to use FindHue without legally required
parental consent. We do not knowingly collect personal information from children under 13. If we
learn that we have done so, we will take appropriate steps to delete it. If you believe a child has
provided us information improperly, contact us using the details below.

## Real-world safety

Playing FindHue means looking for color in the real world. This policy doesn't collect anything
extra from that — no location permission, no sensors beyond the camera you choose to use — but see
the Terms of Use's [Real-world safety and lawful play](/terms#real-world-safety) section and the
[Playing safely](/support#playing-safely) section of Support for the behavior we expect while
playing.

## Changes to this policy

We may update this policy as FindHue changes and will update the "Last updated" date above. Material
changes may receive additional notice. We will request affirmative consent where legally required;
continued use is not treated as consent to every new processing activity.

## Contact {#contact}

Questions about this policy or your data: [support-findhue@edumon.studio](mailto:support-findhue@edumon.studio),
or visit our [Support page](/support) for other ways to reach us.
