# Package Structure

```
security-manager/
├── composer.json
├── README.md
├── LICENSE.md
├── config/
│   └── security-manager.php
├── src/
│   ├── SecurityManagerServiceProvider.php
│   ├── SecurityManager.php
│   ├── Facades/
│   │   └── SecurityManager.php
│   ├── Http/
│   │   ├── Controllers/
│   │   │   └── SecurityManagerController.php
│   │   └── Middleware/
│   │       ├── RateLimiter.php
│   │       ├── GeoBlocker.php
│   │       ├── XssProtection.php
│   │       └── SqlInjectionProtection.php
│   ├── Models/
│   │   ├── SecurityLog.php
│   │   ├── BlockedIp.php
│   │   └── SecuritySetting.php
│   ├── Services/
│   │   ├── GeoLocationService.php
│   │   ├── LoggingService.php
│   │   ├── NotificationService.php
│   │   └── ThreatDetectionService.php
│   ├── Events/
│   │   ├── SecurityThreatDetected.php
│   │   ├── BruteForceDetected.php
│   │   └── SuspiciousActivityDetected.php
│   ├── Listeners/
│   │   ├── LogSecurityThreat.php
│   │   ├── NotifyAdminAboutThreat.php
│   │   └── BlockSuspiciousIp.php
│   └── Console/
│       └── Commands/
│           ├── SecurityScan.php
│           └── CleanLogs.php
├── database/
│   └── migrations/
│       ├── 2023_01_01_000000_create_security_logs_table.php
│       ├── 2023_01_01_000001_create_blocked_ips_table.php
│       └── 2023_01_01_000002_create_security_settings_table.php
├── resources/
│   ├── views/
│   │   ├── dashboard.blade.php
│   │   ├── logs.blade.php
│   │   ├── settings.blade.php
│   │   ├── blocked-ips.blade.php
│   │   └── layouts/
│   │       └── app.blade.php
│   ├── js/
│   │   └── dashboard.js
│   └── css/
│       └── dashboard.css
└── routes/
    └── web.php
```
