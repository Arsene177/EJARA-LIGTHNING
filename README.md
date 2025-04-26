# Bit2Momo Payment App

A simple web application to generate Lightning Network payment invoices for mobile money merchants in Africa. Users can enter merchant details and an amount in FCFA, and the app will generate a Lightning invoice (in SATs) and display a QR code for payment.

## Features
- Enter merchant country and mobile money number
- Enter payment amount in FCFA (West African CFA franc)
- Automatic conversion from FCFA to Satoshis (SATS)
- Generate Lightning Network payment invoice via API
- Display QR code for easy payment
- Show both FCFA and SATS amounts in the receipt
- Simulated merchant verification and payment status

## Setup
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/bit2momo.git
   cd bit2momo
   ```
2. **Open `index.html` in your browser**
   - No build step is required; this is a static HTML/JS project.

## Usage
1. Fill in the merchant's country and mobile money number.
2. Enter the amount in FCFA you wish to pay.
3. Click "Generate Payment Invoice".
4. The app will:
   - Convert the amount to SATs
   - Call the LightningPay API to generate an invoice
   - Display a QR code and payment details
5. Scan the QR code with a Lightning wallet to pay.
6. The app will simulate payment and merchant confirmation.

## API
- Uses the [Ejara LightningPay Testbox API](https://lightningpay-testbox.ejaraapis.xyz/api/v1/invoices) to generate invoices.
- Requires an API key (already included for demo purposes).

## Customization
- To use your own API endpoint or key, edit the fetch URL and headers in `index.html`.
- To add more countries or currencies, update the country selection and conversion rates.

## Dependencies
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [Font Awesome](https://fontawesome.com/) for icons
- [qrcode](https://github.com/soldair/node-qrcode) for QR code generation

## License
MIT 