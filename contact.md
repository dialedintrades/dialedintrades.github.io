---
layout: default
title: Contact
description: "Book a discovery call or send a message to Dialed In Trades."
permalink: /contact/
---

<section class="wrap-narrow page-content" markdown="1">

# Let's talk

The fastest way to start is to book a free discovery call directly.
If you're not ready for that yet, send a message below.

<a class="btn btn-primary btn-large" href="{{ site.booking_url }}">Book a Free Discovery Call</a>

<!--
  Replace the src below with your actual Calendly (or similar) embed URL
  once it's set up. This inline embed keeps the visitor on the site
  instead of sending them away.
-->
<div class="calendly-embed">
  <iframe
    src="https://calendly.com/REPLACE_ME"
    width="100%"
    height="700"
    frameborder="0">
  </iframe>
</div>

## Or send a message

<!--
  This form posts to Formspree. Since GitHub Pages serves static files only,
  a third-party form handler is required. Sign up at formspree.io, create a
  form, and replace YOUR_FORM_ID below with the ID it gives you.
-->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="contact-form">
  <label for="name">Name</label>
  <input type="text" id="name" name="name" required>

  <label for="email">Email</label>
  <input type="email" id="email" name="email" required>

  <label for="phone">Phone</label>
  <input type="tel" id="phone" name="phone">

  <label for="company">Company</label>
  <input type="text" id="company" name="company">

  <label for="trade">Trade</label>
  <select id="trade" name="trade">
    <option value="landscaping">Landscaping</option>
    <option value="irrigation">Irrigation</option>
    <option value="lawn_care">Lawn Care</option>
    <option value="other">Other</option>
  </select>

  <label for="message">What's slowing you down right now?</label>
  <textarea id="message" name="message" rows="5" required></textarea>

  <button type="submit" class="btn btn-primary">Send Message</button>
</form>

<p>Or reach out directly: <a href="mailto:{{ site.contact_email }}">{{ site.contact_email }}</a></p>

</section>
