# Qonaq.ai — AI-powered Property Management System for Kazakhstan

**Live product:** https://qonaq-ai.vercel.app · **Guest booking demo:** https://qonaq-ai.vercel.app/book/kvartirnoe-byuro-ai

> Qonaq (қонақ) means "guest" in Kazakh.

Qonaq.ai is a full-featured PMS built for the underserved market of small hospitality businesses in Kazakhstan — mini-hotels, serviced apartments, and hostels that today run on paper notebooks, Excel, and WhatsApp chats. Global PMS products are too expensive and ignore local realities: Kaspi payments, WhatsApp as the primary booking channel, mandatory e-Qonaq migration reporting for foreign guests, and the Kazakh language.

*This is a showcase repository — the product source code is private. Happy to walk through the codebase or give reviewer access on request.*

## The problem

Kazakhstan has thousands of small accommodation businesses (2–30 units). Their operations live in WhatsApp: guests write to book, send Kaspi payment screenshots, and ask questions. Owners juggle a notebook calendar, lose bookings to double-entry mistakes, have no analytics, and spend hours on manual migration paperwork for foreign guests. Booking.com takes 15–20% commission for the fraction of demand that comes through it.

## What Qonaq.ai does

**For the owner and staff**
- Bookings, calendar grid (chessboard view), guest CRM with loyalty discounts, hourly and daily rates
- Multi-property support with role-based access (owner / manager / reception) and a full audit trail: who changed a booking status, who received a payment, who issued documents
- Finance: mixed payments (cash + Kaspi QR in one booking), expenses per unit, P&L analytics by property and unit, Excel exports
- WhatsApp automation (Green API): booking confirmations, Kaspi payment links, check-in instructions — from editable templates with AI text improvement
- Push notifications (PWA): new booking requests reach staff phones even with the browser closed, with escalating sound reminders until handled
- Kazakhstan-specific: e-Qonaq workflow for foreign guests, business-trip document tracking (fiscal receipts for корпоративные командировочные), 2GIS integration

**For the guest — a public booking page per property**
- Trilingual (Kazakh / Russian / English) with AI-translated descriptions
- Live availability calendar, photo lightbox, dynamic pricing (weekday/weekend, per-guest surcharges, hostel per-bed)
- Smart request form: foreign-citizen flag (triggers registration workflow), business-trip document request, planned arrival time
- Request status tracking page — guests see "received → processing → confirmed" without messaging the hotel

**AI inside**
- Incoming free-text booking requests are parsed by Claude (dates, guest, unit preference) into structured requests
- One-click AI copywriting for unit/property descriptions; automatic KZ/EN translation with database caching
- AI business insights over occupancy, channels, and unit performance

## Tech

Next.js 14 (App Router, TypeScript) · Supabase (Postgres + Auth) · Vercel · Anthropic Claude API · Green API (WhatsApp) · Web Push / PWA

Built and shipped by a solo product manager using AI-assisted development, from first commit to production in under two weeks: 50+ shipped features, daily automated database backups, CI deployment pipeline, and a maintained public backlog.

## Author

**Aizhan Meirbek** — product manager, Kazakhstan
