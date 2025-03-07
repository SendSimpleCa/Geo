# Geo v0.1
Geo is a practical guide and framewrok for understanding and developing html email. 
From the very basics of understanding email rendering and design to using our email boilerplate and a full library of modular snippets. 
Provided by SendSimple.ca

Author - Daniel Sivan

****************************************************************************************************************************
# Introduction

Building emails that look great everywhere isn’t as simple as designing a web page. With so many email clients, screen sizes, and quirks—especially in Outlook—email developers need to take a strategic approach to layout and responsiveness.

Geo by SendSimple.ca seeks to solve development hurdles by providing a modular template system for HTML email makes designing and coding emails faster, more consistent, and easier to maintain. Instead of building each email from scratch, you can use a set of reusable components—like headers, footers, content blocks, and buttons—that can be mixed and matched as needed. This approach not only saves time but also ensures brand consistency and improves responsiveness across different devices. Whether you’re sending a simple newsletter or a complex promotional email, a modular system keeps your workflow efficient and scalable, allowing you to focus on crafting great content rather than wrestling with code.

**Geo by SendSimple.ca will also push the boundaries of email design with animated elements. While traditional email design was mostly static, advanced techniques now allow for CSS animations without relying on JavaScript. These features help create more engaging experiences. When used strategically, these cutting-edge techniques can make emails feel more like engaging and exciting, increasing engagement and click-through rates.**

****************************************************************************************************************************

## **Email Design Approaches** ##


### 1️⃣ Fluid Emails (Uses percentage-based widths) ###

✔ Uses width: 100% or percentages instead of fixed pixels.
✔ Works well in all email clients, even Outlook.
✔ No media queries needed.

Example: 
```
<table role="presentation" width="100%" style="max-width: 600px;">
  <tr>
    <td style="width: 50%;">Left</td>
    <td style="width: 50%;">Right</td>
  </tr>
</table>
```

### 2️⃣ Scalable Emails (Bigger fonts, buttons, easy to tap) ###

✔ Uses bigger fonts, touch-friendly buttons for mobile.
✔ Scales up or down naturally without major layout shifts.
✔ No advanced media queries needed.

Example: 
```
<p style="font-size: 18px; line-height: 1.5;">
  This text is easy to read on all devices.
</p>
<a href="#" style="display: inline-block; padding: 14px 24px; font-size: 20px;">
  Click Me
</a>
```

### 3️⃣ Hybrid (Spongy) Emails (Mix of fixed and fluid elements) ###

✔ Uses max-width + percentage widths for better control.
✔ Works in Outlook without media queries.
✔ More structured than pure fluid layouts.


Example: 
```
<table role="presentation" width="100%" style="max-width: 600px;">
  <tr>
    <td style="width: 49%; max-width: 290px;">Left Column</td>
    <td style="width: 49%; max-width: 290px;">Right Column</td>
  </tr>
</table>
```

### 4️⃣ Mobile-First Emails (Starts with mobile layout) ###

✔ Uses media queries to adjust layout for larger screens.
✔ Defaults to a single-column layout.
✔ Better UX for mobile users.

Example: 
```
<style>
  @media screen and (min-width: 600px) {
    .two-columns { width: 50% !important; }
  }
</style>

<table role="presentation" width="100%">
  <tr>
    <td class="two-columns" style="display: block; width: 100%;">Column 1</td>
    <td class="two-columns" style="display: block; width: 100%;">Column 2</td>
  </tr>
</table>
```

### 5️⃣ Adaptive Emails (Uses media queries to completely change layout) ###

✔ Uses CSS media queries to switch layouts.
✔ Can hide/show content based on screen size.
✔ Gives full control over desktop vs. mobile views..

Example: 
```
<style>
  @media screen and (max-width: 600px) {
    .stack { display: block !important; width: 100% !important; }
  }
</style>

<table role="presentation" width="100%">
  <tr>
    <td class="stack" style="width: 50%;">Column 1</td>
    <td class="stack" style="width: 50%;">Column 2</td>
  </tr>
</table>
```






****************************************************************************************************************************

## Geo's Approach

