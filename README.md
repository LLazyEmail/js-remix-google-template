# js-remix-google-template


https://raw.githubusercontent.com/LLazyEmail/documentation/refs/heads/main/static/templates/google.html

```code

const HeaderStatic = () => {
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="padding: 17px 24px 45px 24px;">
      <a href="https://store.google.com/?utm_source=transactional&utm_campaign=GS100698&utm_medium=email_service&utm_term=storelogo_en-US&utm_content=_100082566_10040889_1572639866037__US__storelogo_en-US" target="_blank" style="text-decoration: none; display: inline-block;">
        <img src="https://www.google.com/images/branding/googleg/2x/googleg_standard_color_32dp.png" alt="Google Store" width="32" style="border: 0; display: block;">
      </a>
    </td>
  </tr>
</table>`;
};


const BannerStatic = () => {
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="padding: 17px 24px 45px 24px;">
      <div style="font-size: 32px; font-weight: bold;">Hi Smiles Davis,</div>
      <p style="margin-top: 8px;">Your shipment was just dropped off. Go on. Open it and enjoy.</p>
    </td>
  </tr>
</table>`;
};

const OrderInfoStatic = () => {
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="padding: 28px 24px 28px 24px; background-color: #f7f7f7;">
      <table width="100%" cellpadding="0" cellspacing="0" style="border-collapse: collapse;">
        <tr>
          <td style="font-weight: bold; font-family: Arial, sans-serif; font-size: 13px; line-height: 16px;">
            Ordered: Oct 24
          </td>
          <td style="width: 20px;"></td> <!-- spacer -->
          <td style="font-weight: bold; font-family: Arial, sans-serif; font-size: 13px; line-height: 16px;">
            Shipped: Oct 30
          </td>
          <td style="width: 20px;"></td> <!-- spacer -->
          <td style="font-weight: bold; font-family: Arial, sans-serif; font-size: 13px; line-height: 16px; text-align: right;">
            Delivered: Nov 01
          </td>
        </tr>
      </table>
    </td>
  </tr>
</table>`;
};

const ProductDetailStatic = () => {
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="vertical-align: top; padding: 10px;">
      <img src="https://lh3.googleusercontent.com/UQdT2kDIPDb65JrhGxh0ViEAe4v-IYH9Ndmo8fGcvyx3dpDq8KxF8wQMKTt0INYQpYjK" width="100" style="border: 0; display: block;">
    </td>
    <td style="vertical-align: top; padding: 10px;">
      <div style="font-family: Arial, sans-serif; font-size: 14px; font-weight: bold;">Google Home Mini (Chalk)</div>
      <div style="font-family: Arial, sans-serif; font-size: 13px; color: #666;">ID: 6500500050</div>
      <div style="font-family: Arial, sans-serif; font-size: 13px;">Price: $49.00</div>
      <div style="font-family: Arial, sans-serif; font-size: 13px;">Quantity: 1</div>
    </td>
  </tr>
</table>`;


const ShippingPaymentStatic = () => {
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="padding: 20px; font-family: Arial, sans-serif; font-size: 13px; color: #666;">
      <strong>Shipping Address:</strong><br>
      Smiles Davis<br>
      600 Montgomery St<br>
      San Francisco, CA 94111<br>
      United States
    </td>
  </tr>
  <tr>
    <td style="padding: 20px; font-family: Arial, sans-serif; font-size: 13px; color: #666;">
      <strong>Payment Method:</strong> Visa •••• 6500
    </td>
  </tr>
</table>`;
};

const FooterStatic = () => {
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; background-color: #eeeeee; margin: 0 auto;">
  <tr>
    <td style="padding: 20px; font-family: Arial, sans-serif; font-size: 12px; color: #666; text-align: center;">
      <p>You have received this service email to update you about your recent Google Store transaction.</p>
      <p>
        <a href="https://accounts.google.com/ServiceLogin" target="_blank" style="color: #666; text-decoration: none;">Account</a> |
        <a href="https://store.google.com/authentication" target="_blank" style="color: #666; text-decoration: none;">Order History</a> |
        <a href="https://support.google.com/store/answer/7334136" target="_blank" style="color: #666; text-decoration: none;">Contact Us</a> |
        <a href="https://store.google.com/intl/en-US_us/about/device-terms.html" target="_blank" style="color: #666; text-decoration: none;">Terms of Sale</a> |
        <a href="https://www.google.com/intl/en/policies/terms/" target="_blank" style="color: #666; text-decoration: none;">Terms of Service</a>
      </p>
      <p>Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043</p>
      <p>&copy; 2019 Google | All Rights Reserved.</p>
    </td>
  </tr>
</table>`;
};


const fullEmailHTML = `
${HeaderStatic()}
${BannerStatic()}
${OrderInfoStatic()}
${ProductDetailStatic()}
${ShippingPaymentStatic()}
${FooterStatic()}
`;


console.log(fullEmailHTML);

```

const Header = (attrs) => {
  const defaultStyles = "padding: 17px 24px 45px 24px;";
  const styleAttr = attrs && attrs.style ? attrs.style + '; ' + defaultStyles : defaultStyles;
  const restAttrs = Object.entries(attrs || {})
    .filter(([k]) => k !== 'style' && k !== 'children')
    .map(([k, v]) => `${k}="${v}"`)
    .join(" ");
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="${styleAttr}">
      <a ${restAttrs} href="https://store.google.com/?utm_source=transactional&utm_campaign=GS100698&utm_medium=email_service&utm_term=storelogo_en-US&utm_content=_100082566_10040889_1572639866037__US__storelogo_en-US" target="_blank" style="text-decoration: none; display: inline-block;">
        <img src="https://www.google.com/images/branding/googleg/2x/googleg_standard_color_32dp.png" alt="Google Store" width="32" style="border: 0; display: block;">
      </a>
    </td>
  </tr>
</table>`;
};
const Banner = (attrs) => {
  const greetingText = attrs && attrs.greeting ? attrs.greeting : "Hi Smiles Davis,";
  const messageText = attrs && attrs.message ? attrs.message : "Your shipment was just dropped off. Go on. Open it and enjoy.";
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="padding: 17px 24px 45px 24px;">
      <div style="font-size: 32px; font-weight: bold;">${greetingText}</div>
      <div style="margin-top: 8px;">${messageText}</div>
    </td>
  </tr>
</table>`;
};


const OrderInfo = (attrs) => {
  // Accepts optional data, e.g.,
  const orderDate = attrs && attrs.orderDate ? attrs.orderDate : "Oct 24";
  const shippedDate = attrs && attrs.shippedDate ? attrs.shippedDate : "Oct 30";
  const deliveryDate = attrs && attrs.deliveryDate ? attrs.deliveryDate : "Nov 01";
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="padding: 28px 24px 28px 24px; background-color: #f7f7f7;">
      <table width="100%" cellpadding="0" cellspacing="0" style="border-collapse: collapse;">
        <tr>
          <td style="font-weight: bold; font-family: Arial, sans-serif; font-size: 13px; line-height: 16px;">
            Ordered: ${orderDate}
          </td>
          <td style="width: 20px;"></td>
          <td style="font-weight: bold; font-family: Arial, sans-serif; font-size: 13px; line-height: 16px;">
            Shipped: ${shippedDate}
          </td>
          <td style="width: 20px;"></td>
          <td style="font-weight: bold; font-family: Arial, sans-serif; font-size: 13px; line-height: 16px; text-align: right;">
            Delivered: ${deliveryDate}
          </td>
        </tr>
      </table>
    </td>
  </tr>
</table>`;
};


const ProductDetail = (attrs) => {
  const imageSrc = attrs && attrs.imageSrc ? attrs.imageSrc : "https://lh3.googleusercontent.com/UQdT2kDIPDb65JrhGxh0ViEAe4v-IYH9Ndmo8fGcvyx3dpD


const ProductDetail = (attrs) => {
  const imageSrc = attrs?.imageSrc ?? "https://lh3.googleusercontent.com/UQdT2kDIPDb65JrhGxh0ViEAe4v-IYH9Ndmo8fGcvyx3dpDq8KxF8wQMKTt0INYQpYjK";
  const productName = attrs?.productName ?? "Google Home Mini (Chalk)";
  const price = attrs?.price ?? "$49.00";
  const quantity = attrs?.quantity ?? 1;

  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="vertical-align: top; padding: 10px;">
      <img src="${imageSrc}" width="100" style="border: 0; display: block;">
    </td>
    <td style="vertical-align: top; padding: 10px;">
      <div style="font-family: Arial, sans-serif; font-size: 14px; font-weight: bold;">${productName}</div>
      <div style="font-family: Arial, sans-serif; font-size: 13px; color: #666;">ID: 6500500050</div>
      <div style="font-family: Arial, sans-serif; font-size: 13px;">Price: ${price}</div>
      <div style="font-family: Arial, sans-serif; font-size: 13px;">Quantity: ${quantity}</div>
    </td>
  </tr>
</table>`;
};

const ShippingPayment = (attrs) => {
  const shippingAddr = attrs?.shippingAddress ?? "Smiles Davis, 600 Montgomery St, San Francisco, CA 94111";
  const paymentMethod = attrs?.paymentMethod ?? "Visa •••• 6500";

  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; margin: 0 auto;">
  <tr>
    <td style="padding: 20px; font-family: Arial, sans-serif; font-size: 13px; color: #666;">
      <strong>Shipping Address:</strong><br>
      ${shippingAddr}
    </td>
  </tr>
  <tr>
    <td style="padding: 20px; font-family: Arial, sans-serif; font-size: 13px; color: #666;">
      <strong>Payment Method:</strong> ${paymentMethod}
    </td>
  </tr>
</table>`;
};

const Footer = (attrs) => {
  // You can pass links or info as attrs for customization if needed
  return `
<table width="600" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 600px; background-color: #eeeeee; margin: 0 auto;">
  <tr>
    <td style="padding: 20px; font-family: Arial, sans-serif; font-size: 12px; color: #666; text-align: center;">
      <p>You have received this service email to update you about your recent Google Store transaction.</p>
      <p style="margin: 10px 0;">
        <a href="https://accounts.google.com/ServiceLogin" target="_blank" style="color: #666; text-decoration: none;">Account</a> |
        <a href="https://store.google.com/authentication" target="_blank" style="color: #666; text-decoration: none;">Order History</a> |
        <a href="https://support.google.com/store/answer/7334136" target="_blank" style="color: #666; text-decoration: none;">Contact Us</a> |
        <a href="https://store.google.com/intl/en-US_us/about/device-terms.html" target="_blank" style="color: #666; text-decoration: none;">Terms of Sale</a> |
        <a href="https://www.google.com/intl/en/policies/terms/" target="_blank" style="color: #666; text-decoration: none;">Terms of Service</a>
      </p>
      <p style="margin: 10px 0;">Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043</p>
      <p style="margin: 10px 0;">&copy; 2019 Google | All Rights Reserved.</p>
    </td>
  </tr>
</table>`;
};


const emailHtml = `
${Header({ style: "padding: 20px; background-color: #fff;" })}
${Banner({ greeting: "Hello John!", message: "Your order has shipped." })}
${OrderInfo({ orderDate: "Oct 24", shippedDate: "Oct 25", deliveryDate: "Oct 30" })}
${ProductDetail({ imageSrc: "https://example.com/product.jpg", productName: "Awesome Product", price: "$99" })}
${ShippingPayment({ shippingAddress: "123 Main St", paymentMethod: "MasterCard •••• 1234" })}
${Footer() }
`;
console.log(emailHtml);



