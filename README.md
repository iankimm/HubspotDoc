<h1> Melissa API Express Entry to HubSpot Form </h1>

<section>
<div>
  <h2> Contents </h2>
</div>
<nav aria-label="Page">
<ul class="visible nav section-nav flex-column">
<li class="toc-h2 nav-item toc-entry"><a class="reference internal nav-link" href="#introduction">Introduction</a></li>
<li class="toc-h2 nav-item toc-entry"><a class="reference internal nav-link" href="#requirements">Requirements</a></li>
<li class="toc-h2 nav-item toc-entry"><a class="reference internal nav-link" href="#getting-started">Getting Started</a><ul class="nav section-nav flex-column">
<li class="toc-h3 nav-item toc-entry"><a class="reference internal nav-link" href="#steps">Steps</a><ul class="nav section-nav flex-column">
<li class="toc-h4 nav-item toc-entry"><a class="reference internal nav-link" href="#step1">1. Preparation</a></li>
<li class="toc-h4 nav-item toc-entry"><a class="reference internal nav-link" href="#step2">2. Creating HubSpot Form</a></li>
<li class="toc-h4 nav-item toc-entry"><a class="reference internal nav-link" href="#step3">3. Creating HubSpot Landing Page</a></li>
<li class="toc-h4 nav-item toc-entry"><a class="reference internal nav-link" href="#step4">4. Configuration</a></li>
<li class="toc-h4 nav-item toc-entry"><a class="reference internal nav-link" href="#step5">5. Finish</a></li>
</ul>
</section>
  
<section id="introduction">
<h2><a class="toc-backref" href="#id11" role="doc-backlink">Introduction</a><a class="headerlink" href="#introduction" title="Link to this heading"></a></h2>
<p>This guide provides detailed instructions for integrating Melissa's Express Entry service, an auto-complete address verification tool, with HubSpot. </p>
<o>Since HubSpot does not natively support the integration of external APIs within its forms, this solution utilizes a landing page that functions as a form. 
The landing page will collect address data through Melissa's Express Entry service, automatically verifying and completing fields such as city, state, and postal code, while reducing manual entry by up to 50%.
The data entered on the landing page will then be exported and imported into HubSpot form submissions, ensuring accurate and efficient data capture.</p>

</section>

<section id="requirements">
<h2><a class="toc-backref" href="#id11" role="doc-backlink">Requirements</a><a class="headerlink" href="#requirements" title="Link to this heading"></a></h2>
<ul>
  <li>HubSpot account with landing page and form</li>
  <li>Access to Melissa Express Entry</li>
</ul>
</section>

<section id="getting-started">
<h2><a class="toc-backref" href="#id13" role="doc-backlink">Getting Started</a><a class="headerlink" href="#getting-started" title="Link to this heading"></a></h2>
  
<section id="steps">
<h3><a class="toc-backref" href="#id14" role="doc-backlink">Steps</a><a class="headerlink" href="#steps" title="Link to this heading"></a></h3>

<section id="step1">
  <h4><a class="toc-backref" href="#id15" role="doc-backlink">1. Preparation</a><a class="headerlink" href="#step1" title="Link to this heading"></a></h4>

  <p>The preparation phase is divided into two key tasks: creating a landing page and creating a form. Both tasks require access to the Landing Pages and Forms sections within HubSpot.</p>

  <h5>Part 1: Creating a New Landing Page</h5>
  <ol>
    <li><strong>Log into HubSpot</strong><br>
      Begin by logging into your HubSpot account. Navigate to the Content section in the main navigation menu.
    </li>
    <li><strong>Access Landing Pages</strong><br>
      From the left-hand panel, select Landing Pages under the Content menu.
    </li>
    <li><strong>Create a New Landing Page</strong><br>
      On the Landing Pages page, click the Create button (located in the top right corner of the page). This will initiate the landing page creation process.
    </li>
    <li><strong>Select Website and Name the Landing Page</strong><br>
      In the creation dialog, you will be prompted to select the website that the landing page will be associated with. Afterward, enter a descriptive and identifiable name for the landing page. Ensure that the name clearly reflects the purpose of the page for easy reference.<br>
      This landing page will serve as a form and will be used to collect user submissions for HubSpot Forms.
    </li>
  </ol>

  <h5>Part 2: Creating a New Form</h5>
  <ol>
    <li><strong>Navigate to Forms</strong><br>
      Once the landing page is created, move to the Marketing section in the left-hand navigation menu. Under Marketing, select Forms.
    </li>
    <li><strong>Create a New Form</strong><br>
      Similar to the landing page creation process, click on the Create Form button located in the top right corner.
    </li>
    <li><strong>Choose the Form Type</strong><br>
      HubSpot will offer different form creation options. For a simple, pre-populated form with predefined fields, select the Legacy Editor option. This allows you to create a form based on HubSpot's default templates, streamlining the setup process.
    </li>
    <li><strong>Configure Form Fields</strong><br>
      Follow the guided steps provided by HubSpot to add the necessary fields for your form. Essential fields for your specific use case (to utilize Melissa Express Entry) include:
      <ul>
        <li>Street Address</li>
        <li>City</li>
        <li>State</li>
        <li>Zip Code</li>
        <li>Country</li>
      </ul>
      These fields will enable you to capture the required data for integration with Melissa Express Entry on your landing page.
    </li>
  </ol>
</section>

<section id="step2">
<h4><a class="toc-backref" href="#id15" role="doc-backlink">2. Creating HubSpot Form</a><a class="headerlink" href="#step2" title="Link to this heading"></a></h4>
UNDER CONSTRUCTION!
</section>

<section id="step3">
  <h4><a class="toc-backref" href="#id15" role="doc-backlink">3. Creating HubSpot Landing Page</a><a class="headerlink" href="#step3" title="Link to this heading"></a></h4>

  <p>In this step, we will configure the HubSpot landing page created in Step 1 to display page like a form. The process involves removing the default content automatically populated by HubSpot and replacing it with the form fields you set up in Step 2.</p>

  <h5>1. Remove Default Content</h5>
  <p>Navigate to the HubSpot landing page you created in Step 1. By default, HubSpot may have populated the landing page with pre-existing content. To begin, delete this default content to ensure that the page is empty and ready for your custom form.</p>

  <h5>2. Add a Rich Text Module</h5>
  <p>Next, locate the left-side panel and click on the <strong>+ (Add to Page)</strong> button. From the options available, search for <strong>Rich Text</strong> and drag it onto the landing page. This module will allow you to add custom HTML content.</p>

  <h5>3. Access the Source Code</h5>
  <p>Click on the newly added <strong>Rich Text</strong> box to open its settings. In the top-right corner of the settings menu, look for the <strong>Advanced Options</strong> dropdown, and select <strong>Source Code</strong>. This will enable you to insert custom HTML code directly into the page.</p>

  <h5>4. Add the Custom Form HTML</h5>
  <p>In the <strong>Source Code</strong> view, you can now input the HTML code for the form fields you created in Step 2. Below is an example HTML form code that corresponds to the fields you configured earlier for example. Ensure the input IDs and descriptions align with your form setup:</p>

  <pre><code>
  &lt;form&gt;
    &lt;h3&gt;Example Form&lt;/h3&gt;
    First Name &lt;input id="firstName" type="text"&gt; 
    Last Name &lt;input id="lastName" type="text"&gt; 
    Phone Number &lt;input id="phoneNumber" type="text"&gt; 
    Email &lt;input id="email" type="text"&gt; 
    Address Line 1 &lt;input id="addressLine1" type="text"&gt; &lt;span id="suggestions"&gt;&lt;/span&gt; 
    Address Line 2 &lt;input id="addressLine2" type="text"&gt; 
    City &lt;input id="city" type="text"&gt; 
    State &lt;input id="state" type="text"&gt; 
    Zip Code &lt;input id="zipCode" type="text"&gt; 
    Country &lt;input id="country" type="text"&gt; 
    &lt;button id="submitButton"&gt;SUBMIT&lt;/button&gt;
  &lt;/form&gt;
  </code></pre>
  <a href="https://github.com/iankimm/HubspotDoc/blob/main/richtext.html">Code File</a>
  <p><strong>Note:</strong> You should modify the above HTML code to match the specific input IDs and field names from your form. Ensure that the input IDs are correctly mapped to your HubSpot form fields.</p>
  
  <h5>5. Implement Address Suggestions</h5>
  <p>Particularly for the <strong>Address Line 1</strong> field, keep the <code>&lt;span id="suggestions"&gt;&lt;/span&gt;</code> element active. This will be used later to integrate address suggestions from <strong>Melissa Express Entry</strong>, providing users with accurate address data as they type.</p>

  <h5>6. Save the Changes</h5>
  <p>Once you've inserted and adjusted the HTML code to your satisfaction, be sure to save the changes. This will make the custom form live on the landing page, ready to collect user submissions.</p>

</section>

<section id="step4">
  <h4><a class="toc-backref" href="#id15" role="doc-backlink">4. Configuration</a><a class="headerlink" href="#step4" title="Link to this heading"></a></h4>

  <p>In this step, we will configure the backend functionality for the form set up in Step 3. This involves adding necessary code to the footer HTML of the landing page to enable the proper working of the form's backend processes.</p>

  <h5>1. Accessing the Footer HTML Section</h5>
  <p>To begin, navigate to the settings of the landing page you're currently editing. Specifically, you need to access the <strong>Footer HTML</strong> section, where we will be integrating the backend code for the form functionalities. Follow these steps:</p>
  <ol>
    <li>Open the landing page settings.</li>
    <li>Go to the <strong>Advanced</strong> tab.</li>
    <li>Locate the <strong>Footer HTML</strong> field.</li>
  </ol>

  <h5>2. Preparing the Code</h5>
  <p>Before pasting the provided backend code into the Footer HTML, there are several important considerations to ensure everything works as expected:</p>
  <ol>
    <li><strong>Customizing for Your Form:</strong> The code you are about to integrate is designed to work with the example form provided in Step 3. If your form differs from the example, you may need to modify the code to match your specific form fields (e.g., input IDs, field names, or validation logic).</li>
    <li><strong>Review Dependencies:</strong> Ensure that any third-party integrations, such as Melissa Express Entry or other services, are properly set up and referenced within the code.</li>
    <li><strong>Testing:</strong> It is crucial to test the code thoroughly in a development environment before applying it to the live landing page. This ensures that all backend functionalities, such as form submission handling, data validation, and integration with external services, work as expected.</li>
  </ol>

  <h5>3. Adding the Code to the Footer HTML</h5>
  <p>Once you have reviewed and prepared the code, you can proceed to paste it into the Footer HTML section. This will allow the form to perform necessary functions, such as processing submissions and interacting with the services configured earlier (e.g., Melissa Express Entry). Ensure that the code is placed correctly, without interrupting other elements of the page.</p>

  <h5>4. Finalizing the Configuration</h5>
  <p>After pasting the code and ensuring everything is configured, be sure to save the changes. Once saved, the landing page will be fully configured to handle form submissions with the necessary backend logic in place.</p>

  <p><strong>Note:</strong> It is highly recommended to conduct thorough testing after applying the configuration to confirm that the form functionalities are working seamlessly, especially for integrations with external services like Melissa Express Entry.</p>

</section>

<section id="step5">
<h4><a class="toc-backref" href="#id15" role="doc-backlink">5. Finish</a><a class="headerlink" href="#step5" title="Link to this heading"></a></h4>
UNDER CONSTRUCTION
</section>
  
</section>

</section>
