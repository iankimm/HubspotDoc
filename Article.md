# Integrating Melissa’s Express Entry with HubSpot Landing Pages

Some of the most powerful tools marketers use are forms. We rely on them to collect valuable data, offer free trials, and gather customer information. But let's face it—getting validated addresses for direct mail campaigns or other CRM activities has been a hassle until now.

If you're running a business like lawn care, or need to collect accurate addresses for routing and districting, you probably used an open text field in your forms. But we all know what that leads to—incorrect data, typos, and even fake addresses. 

The good news? That’s about to change.

With **Melissa's Express Entry** integration, you can create a smooth user experience that **auto-completes** addresses and validates them as users type. Here's how to integrate this with HubSpot using a custom landing page.

## Why Not Use HubSpot's Native Form?

While HubSpot’s form builder is great, it doesn't allow direct integration with external services like **Melissa Express Entry**. According to HubSpot’s support: 

> "If you’re using HubSpot's default form builder, you can’t directly edit the form's HTML or JavaScript within the HubSpot interface."

But don’t worry. We can bypass this limitation by embedding a custom HTML form on a **landing page** and using **JavaScript** to interact with the Melissa Express Entry API. This way, we can still integrate the form with HubSpot CRM, and you’ll get a slick user experience.

## What You'll Need

- **HubSpot** account
- **Melissa Express Entry** API key
- Basic HTML and JavaScript skills (don’t worry, we’ve got you covered)

## Steps to Implement the Solution

### Step 1: Set Up Your HubSpot Landing Page and Form

#### 1.1 Create a New Landing Page
- Log into HubSpot and go to **Content > Landing Pages**.
- Click **Create** in the top-right corner.
- Name your landing page (e.g., "Address Verification Form").

#### 1.2 Create the HubSpot Form
- Go to **Marketing > Forms** and click **Create Form**.
- Use the **Legacy Editor** and add the following fields:
  - First Name
  - Last Name
  - Email Address
  - Address Line 1
  - Address Line 2
  - City
  - State
  - Zip Code
  - Country

These fields will correspond with the Melissa Express Entry service for address validation.

---

### Step 2: Building the Custom Landing Page Form

Now, we’re going to add the form to your landing page using **HTML**.

#### 2.1 Remove Default Content
By default, HubSpot may populate your landing page with pre-existing content. Simply **delete** this content.

#### 2.2 Add a Rich Text Module
- From the left sidebar, drag a **Rich Text** module to where you want your form to appear.
- Click on **Source Code** in the module settings and paste the following HTML form code:

```html
<form>
  <h3>Address Verification Form</h3>
  First Name <input id="firstName" type="text">
  Last Name <input id="lastName" type="text">
  Phone Number <input id="phoneNumber" type="text">
  Email <input id="email" type="text">
  Address Line 1 <input id="addressLine1" type="text"> <span id="suggestions"></span>
  Address Line 2 <input id="addressLine2" type="text">
  City <input id="city" type="text">
  State <input id="state" type="text">
  Zip Code <input id="zipCode" type="text">
  Country <input id="country" type="text">
  <button id="submitButton">Submit</button>
</form>
```

#### 2.3 Save the Page
Once your form is set up, **save** the page. This is where the auto-complete magic will happen.

---

### Step 3: Add the Backend Code

Now, we need to add the **JavaScript code** that will integrate **Melissa Express Entry** with your form.

#### 3.1 Access the Footer HTML Section
- Go to the settings of your landing page.
- Under the **Advanced** tab, locate the **Footer HTML** section.

#### 3.2 Add the Backend Code
Before you add the backend code:
- Make sure you’ve **updated** the form fields to match the ones in the page.
- Ensure you’ve **referenced** the **Melissa Express Entry API** in your script.

#### 3.3 Paste the JavaScript Code
Paste your custom **backend code** into the **Footer HTML** section. This code will enable the form to interact with the **Melissa Express Entry API** for real-time address validation.

#### 3.4 Save and Test
Once everything is saved, **test** your form by typing an address. You should see **suggestions** populate as users type.

---

### Step 4: Finalize and Go Live

Now that everything is set up, it's time to finalize:

- **Publish** your landing page.
- **Test** the form thoroughly to ensure it’s capturing data correctly and verifying addresses.

Once you're confident it’s working smoothly, you’re all set!

---

### Conclusion: Error-Free Address Forms, Finally!

And there you have it—a fully functional address verification system integrated with **Melissa Express Entry** on a HubSpot landing page. No more dealing with invalid addresses or data entry mistakes. Your users will experience a seamless form with real-time address suggestions, and your CRM will get clean, verified data every time.

So, go ahead—**test it**, **tweak it**, and get ready to say goodbye to messy address data!