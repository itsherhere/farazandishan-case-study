# Engineering Decisions

## Keep the existing backend
The project integrates with the client's existing GraphQL backend instead of replacing it. This avoids duplicating business logic and keeps the existing system as the source of truth.

## Use Sanity only for editorial content
Sanity is used for public content that editors need to manage. Protected operational functionality remains outside the CMS.

## Use a server-side integration layer
Next.js server-side code mediates backend calls so UI components can work with normalized application data instead of backend-specific response shapes.

## Share structure across Persian and English
Locale-prefixed routes keep localization explicit while allowing both languages to share components and information architecture.

## Validate production builds continuously
Type-checking, linting, Next.js builds, and Sanity Studio builds are treated as part of the normal engineering workflow rather than final cleanup.
