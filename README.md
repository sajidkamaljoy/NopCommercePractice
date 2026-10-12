# NopCommercePractice

A practice workspace built on [nopCommerce](https://www.nopcommerce.com/) **4.70.3**, used for learning and experimenting with nopCommerce plugin development, payments and real-time features.

## What's in this repo

- The full nopCommerce solution (`NopCommerce.sln`): `Libraries`, `Presentation` (`Nop.Web`, `Nop.Web.Framework`), `Plugins`, `Tests` and the `Build` scripts.
- The standard nopCommerce plugins (PayPal Commerce, UPS, Avalara, Google Analytics, Facebook Pixel, Brevo, Omnisend and others).
- nopStation and practice plugins added on top:

| Plugin | Purpose |
|---|---|
| `NopStation.Plugin.Payments.StripeHostedCheckout` | Payment method that sends customers to Stripe Hosted Checkout |
| `NopStation.Plugin.Misc.Core` | Shared base plugin that manages nopStation plugins |
| `NopStation.Plugin.Misc.FacebookShop` | Imports the catalog into a Facebook shop |
| `NopStation.Plugin.Theme.MikesChainsaw` | Storefront theme with configurable settings |
| `Nop.Plugin.Widget.NopStationEmployees` | Widget that lists nopStation employees, and the place where SignalR was added |

## Tech stack

ASP.NET Core, C#, SQL Server, Razor views, Stripe.net, SignalR (client library in the Employees widget).

## Run it

1. Open `NopCommerce.sln` in Visual Studio (with .NET 8 support).
2. Set `Nop.Web` as the startup project and run it.
3. On first launch, complete the installation wizard with a local SQL Server connection.
4. In the admin area, go to **Configuration → Local plugins** to install and enable the plugins above. Stripe needs your own Stripe API keys, which you enter in the plugin's configuration page. Never commit them.

See `Deploying.Readme.txt` for deployment notes, and the [official docs](https://docs.nopcommerce.com/) for the platform.

## License

nopCommerce is distributed under its own license. See `LICENSE.md`.
