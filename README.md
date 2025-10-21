# Gold Ornament Quotation & Price Predictor 💎

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://gold-quotation-app.streamlit.app/)

## 🌟 Features

A comprehensive, multi-language gold ornament prediction and quotation system designed for transparency and accessibility.

### Core Functionality

- **Real-time Gold API Integration** 🔄
  - Support for both free (Metals API) and paid (GoldAPI.io) services
  - Configurable base currency (INR, USD, AED, EUR)
  - Automatic rate caching with 10-minute TTL

- **Modular Price Calculation** 💰
  - Gold value based on weight, karat, and purity
  - Making charges (percentage-based with minimum threshold)
  - Stone costs
  - Hallmarking fees
  - Shipping & insurance
  - Certification & conversion fees
  - GST calculation
  - Discount application
  - Advance payment deduction
  - Final lock band adjustment

- **Multi-language Support** 🌍
  - English, Hindi, Tamil, Telugu, Kannada, Malayalam
  - Marathi, Bengali, Gujarati, Urdu, Arabic
  - French, German
  - Script conversion for Indian and international languages

- **Product Catalogue** 📦
  - Pre-loaded sample jewellery catalogue
  - Searchable and filterable table
  - SKU-based quick quotation
  - Image preview support

- **Upload & OCR** 📸
  - Customer photo upload (PNG, JPG, JPEG, PDF)
  - OCR text extraction (Tesseract-ready)
  - Design image processing

- **PDF/OCR Output** 📄
  - Comprehensive quotation PDF generation
  - Price breakdown with all components
  - Terms & Conditions in selected language
  - Customer information header

- **Business Transparency** ✨
  - Detailed price breakdown display
  - Inspired by industry best practices (Kalyan, Lalitha, JoyAlukkas)
  - Clear component-wise pricing
  - Accessibility-optimized UI

### Accessibility Features

- High contrast colors
- Tab navigation support
- Clear data table labels
- ARIA-compliant elements
- Screen reader friendly

## 🚀 Quick Start

### Local Development

```bash
# Clone repository
git clone https://github.com/ganeshgowri-ASA/gold-ornament-quotation-app.git
cd gold-ornament-quotation-app

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run streamlit_app.py
```

### Configuration

1. **API Keys**: Enter your gold rate API key in the sidebar
   - Free: [Metals API](https://metals-api.com/)
   - Paid: [GoldAPI.io](https://www.goldapi.io/)

2. **Business Parameters**: Adjust in sidebar
   - Making percentage and minimum
   - Hallmarking, shipping, certification fees
   - Insurance and discount percentages
   - GST rate

## 📊 Application Structure

### Navigation Tabs

1. **Home**: Real-time gold rate display and API metadata
2. **Quotation**: Interactive price calculator with detailed breakdown
3. **Catalogue**: Browse and select from sample jewellery items
4. **Upload & OCR**: Upload customer photos or design images
5. **Testimonials/Info**: Application information and accessibility notes

### Price Calculation Logic

```python
Final Payable = (
    (Gold Value + Making Charges + Stone Cost + 
     Hallmarking + Shipping + Certification + Conversion) * 
    (1 + Insurance %) * (1 - Discount %) * (1 + GST %) + 
    Final Lock Band - Advance Paid
)
```

Where:
- **Gold Value** = Weight (g) × Rate per gram × Purity (karat/24)
- **Making Charges** = max(Making Min, Gold Value × Making %)

## 🛠️ Technology Stack

- **Framework**: Streamlit
- **Data Processing**: Pandas, NumPy
- **Image Processing**: Pillow, PyTesseract (OCR)
- **PDF Generation**: ReportLab
- **Translation**: googletrans
- **API Calls**: requests

## 📝 Requirements

See [requirements.txt](requirements.txt) for complete dependency list.

## 🔒 Security & Privacy

- API keys entered via password-protected input
- No data persistence on server
- Session-based state management
- User data not stored or transmitted

## 🎯 Use Cases

- Jewellery retail shops
- Online gold ornament stores
- Customer quotation systems
- Price transparency tools
- Multi-location jewellery chains
- Export-oriented units

## 📖 References

Pricing logic inspired by leading Indian jewellers:
- Kalyan Jewellers
- Lalitha Jewellery
- JoyAlukkas

## ⚠️ Disclaimer

This demo app is for educational purposes. Verify all rates, taxes, and calculations as per local laws and regulations before commercial use.

## 🤝 Contributing

Contributions welcome! Please open an issue or submit a pull request.

## 📧 Contact

For questions or support, please open an issue on GitHub.

## 📄 License

MIT License - feel free to use for educational or commercial purposes.

---

**Built with ❤️ using Streamlit**
