# Integrating Melissa’s Express Entry with HubSpot Landing Pages

Collecting accurate address data is critical yet challenging due to typos, incomplete entries, or false information. By integrating **Melissa’s Express Entry** with your **HubSpot landing page**, you enable real-time address auto-completion and validation, ensuring clean, accurate data flows directly into your CRM.

---

## Why Not Use HubSpot's Native Form?

Before we dive in, let’s address the elephant in the room. HubSpot’s native form builder is fantastic in a lot of ways, but it doesn’t allow for direct integration with external services like **Melissa Express Entry**. To quote HubSpot’s support team directly:

> "If you’re using HubSpot's default form builder, you can’t directly edit the form's HTML or JavaScript within the HubSpot interface."

Okay, so what does this mean for us? It means that we can’t just slap an API into the default HubSpot form and call it a day. But don’t worry — we’re about to get creative.

Instead of relying on HubSpot’s default form, we’ll bypass the limitations and embed a **custom HTML form** into your landing page. With a bit of JavaScript magic, we’ll connect this form to the **Melissa Express Entry API**, enabling real-time address validation. The best part? The form will still connect to your HubSpot CRM, so all the data ends up in the right place.

---

## What You’ll Need:
- A **HubSpot account**
- An **API key** for **Melissa Express Entry**
- Basic knowledge of **HTML** and **JavaScript** (don’t worry, we’ll guide you step-by-step)

---

## Steps to Implement the Solution

### Step 1: Set Up Your HubSpot Landing Page and Form

**1.1 Create a New Landing Page**

- Log into HubSpot and navigate to **Content > Landing Pages**.
- Click **Create** in the top-right corner.
- Name your landing page something catchy — perhaps "Address Verification Form" or "Where Do You Live? We’re Not Stalking You."

## 1.2 Create the HubSpot Form

Next, create the form that will collect data from your users:

- Navigate to **Marketing > Forms** in HubSpot.  
- Click **Create Form** and select the **Legacy Editor**.  
- Add the following fields:

  - Address Line 1  
  - Address Line 2  
  - City  
  - State  
  - Zip Code  
  - Country  

These fields are essential for proper integration with **Melissa Express Entry**, ensuring real-time address validation.  

You may also choose to include commonly used fields like **First Name**, **Last Name**, **Phone Number**, and **Email Address**—while not required for address validation, they are standard in most lead capture forms.

---

## Step 2: Building the Custom Landing Page Form

Now, let’s move on to embedding your custom form directly into a landing page using HTML.

### 2.1 Remove Default Content

Start by removing any default content on the landing page to create a blank canvas.

### 2.2 Add a Rich Text Module

- Drag a **Rich Text module** to the desired section of your landing page.  
- Click **Source Code** in the module settings and paste the following HTML:

```html
<form>
  <h3>Address Verification Form</h3>
  <!-- Optional Fields -->
  First Name <input id="firstName" type="text">
  Last Name <input id="lastName" type="text">
  Phone Number <input id="phoneNumber" type="text">
  Email <input id="email" type="text">
  
  <!-- Essential Address Fields -->
  Address Line 1 <input id="addressLine1" type="text"> <span id="suggestions"></span>
  Address Line 2 <input id="addressLine2" type="text">
  City <input id="city" type="text">
  State <input id="state" type="text">
  Zip Code <input id="zipCode" type="text">
  Country <input id="country" type="text">

  <button id="submitButton">Submit</button>
</form>
```

<a href="https://github.com/iankimm/HubspotDoc/blob/main/richtext.html">Code File</a>

**2.3 Save the Page**

Once your form is in place, **save the page**. The auto-complete magic will start happening here — as users type, address suggestions will start popping up.

---

### Step 3: Add the JavaScript Code

We’re almost there! Now, we need to add the **JavaScript code** that will integrate **Melissa Express Entry** with your form.

**3.1 Access the Footer HTML Section**

- Go to the settings of your landing page.
- Under the **Advanced** tab, find the **Footer HTML** section.

**3.2 Add the JavaScript Code**

Before adding the JavaScript code, make sure to:
- **Update the form fields** to match what you’ve used on the page.
- **Reference the Melissa Express Entry API** in your script.

**3.3 Paste the JavaScript Code**

Now, **paste your custom code** into the **Footer HTML** section. This code will ensure the form interacts with **Melissa Express Entry**, enabling real-time address validation.
<a href="https://github.com/iankimm/HubspotDoc/blob/main/setting.html">Code File</a>

**3.4 Save and Test**

Once everything is saved, it’s time to **test**. Start typing an address and see if the suggestions populate as users type. Magic, right?

---

### Step 4: Finalize and Go Live

You’re nearly there! Time to get everything ready for the real world.

- **Publish** your landing page.
- **Test** the form thoroughly to ensure it’s capturing data correctly and validating addresses as expected.

Once everything looks good and is functioning smoothly, you’re ready to go live!

---

### Conclusion: Error-Free Address Forms, Finally!!

And there you have it — a **fully functional address verification system** integrated with **Melissa Express Entry** on a **HubSpot landing page**. Say goodbye to typos, incorrect addresses, and fake data. Your users will have a seamless experience with real-time address suggestions, and your CRM will get clean, validated data every time.

It’s a win-win for everyone! Go ahead, **test it**, **tweak it**, and enjoy the satisfaction of never having to deal with messy address data again.
This version is now formatted for a GitHub README.md file and includes the necessary markdown syntax 