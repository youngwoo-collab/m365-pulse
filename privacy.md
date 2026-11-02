# M365 Pulse — Privacy Policy

_Last updated: 2026-11-02_

M365 Pulse is a desktop and mobile monitoring app that checks whether Microsoft 365 services
(mail, Teams, SharePoint) work for the person running it. It runs entirely on the user's own
device. There is no M365 Pulse server, no account system, and no analytics.

## What the app accesses

### Google account (optional, "external mail" checks)

If you connect a personal Gmail account, the app asks for two scopes:

| Scope | Why |
|---|---|
| `https://www.googleapis.com/auth/gmail.send` | Send a short automated test message from the connected Gmail account to your Microsoft 365 mailbox, to check that mail from outside Microsoft 365 is delivered. |
| `https://www.googleapis.com/auth/gmail.modify` | Find the app's own test message (by its unique subject) in the connected account, read its message headers to check delivery, and move that test message to Trash afterwards. |

The app only touches messages that it created itself, identified by a unique test subject. It
does not read, list, display, copy or store any other message, contact or attachment, and it
does not read message bodies of other mail.

### Microsoft 365 account

The app signs in to your Microsoft 365 account with Microsoft's own sign-in and uses Microsoft
Graph to send, find and delete its own test items, and to read Microsoft's published service
health. It does not read your other mail, files or messages.

## What is stored, and where

All data stays on your device.

- **Sign-in tokens** (the Google refresh token and Microsoft sign-in state) are kept in the
  operating system's secure store (Windows Credential/DPAPI, Apple Keychain, Android Keystore).
  They are never written to logs, exported files or the local database in readable form.
- **Test results** (time, pass/fail, duration, a normalized error category) are kept in a
  local database on your device.
- **Addresses and identifiers of test items** are stored encrypted (AES-256-GCM); the key is
  in the operating system's secure store.
- **Logs and diagnostic exports** do not contain tokens, email addresses, message content or
  file content.

## What is shared

Nothing is shared with the developer or any third party. The app communicates only with
Google's APIs (for the connected Gmail account) and Microsoft's APIs (for your Microsoft 365
account), directly from your device. The app does not sell, transfer or use Google user data
for advertising, and does not use it to train AI or machine-learning models.

## Google API Services User Data Policy

The use and transfer to any other app of information received from Google APIs will adhere to
the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Retention and deletion

- Test messages are deleted (Gmail: moved to Trash) by the app right after each check. Any
  that could not be removed are retried for up to 24 hours.
- Disconnecting the Gmail account in the app deletes the stored Google credential from your
  device.
- You can also revoke the app's access at any time at
  <https://myaccount.google.com/permissions>.
- Removing the app and its local data folder deletes all remaining local data.

## Children

The app is a monitoring tool for administrators and is not directed at children.

## Changes

If this policy changes, the date above is updated.

## Contact

<!-- Replace with a contact address before publishing. -->
Contact: `coveyi@gmail.com`

---

# M365 Pulse — 개인정보처리방침 (요약)

M365 Pulse는 사용자 본인의 장치에서만 동작하는 Microsoft 365 상태 점검 앱입니다.
별도의 서버, 회원 가입, 분석 도구가 없습니다.

- **Gmail 연결(선택):** 외부 메일 수신 점검을 위해 `gmail.send`(테스트 메일 발송)와
  `gmail.modify`(앱이 보낸 테스트 메일을 제목으로 찾아 헤더를 확인하고 휴지통으로 이동)
  범위를 요청합니다. 앱이 직접 만든 테스트 메일 외의 메일은 읽거나 저장하지 않습니다.
- **저장 위치:** 모든 데이터는 장치 안에만 있습니다. 로그인 token은 OS 보안 저장소에
  보관되며 로그, 내보내기 파일, DB에 평문으로 남지 않습니다. 테스트 항목의 주소·식별자는
  암호화되어 저장됩니다.
- **제3자 제공:** 없습니다. 개발자나 제3자에게 전송하지 않으며, 광고나 AI 학습에 쓰지 않습니다.
- **삭제:** 테스트 메일은 점검 직후 삭제(휴지통 이동)됩니다. 앱에서 Gmail 연결을 해제하면
  저장된 자격 증명이 삭제되고, <https://myaccount.google.com/permissions>에서 언제든
  접근 권한을 철회할 수 있습니다.
- **문의:** `coveyi@gmail.com`
