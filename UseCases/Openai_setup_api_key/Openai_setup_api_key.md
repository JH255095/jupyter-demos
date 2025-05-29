---
jupyter:
  kernelspec:
    display_name: Teradata SQL
    language: Teradata SQL
    name: teradatasql
  language_info:
    codemirror_mode: Teradata SQL
    file_extension: .tdrs
    mimetype: application/vnd.teradata.resultset
    name: Teradata SQL
    version: 16.20
  nbformat: 4
  nbformat_minor: 5
---

<div class="cell markdown">

<header>
   <p  style='font-size:36px;font-family:Arial; color:#F0F0F0; background-color: #00233c; padding-left: 20pt; padding-top: 20pt;padding-bottom: 10pt; padding-right: 20pt;'>
       Using ClearScape Analytics with OpenAI
  <br>
       <img id="teradata-logo" src="https://storage.googleapis.com/clearscape_analytics_demo_data/DEMO_Logo/teradata.svg" alt="Teradata" style="width: 125px; height: auto; margin-top: 20pt;">
    </p>
</header>

<hr style="height:2px;border:none;">    
    

<p style = 'font-size:20px;font-family:Arial;'><b>Introduction:</b></p>
</div>

<div class="cell markdown">

<p style = 'font-size:16px;font-family:Arial;'>To ensure optimal utilization of the OpenAI API in generative AI notebooks, it is essential to establish the API keys correctly. This concise guide outlines the process of configuring OpenAI API keys for seamless integration across multiple notebooks.  This notebook is called by other notebooks that use OpenAI for get the api key. Please note that the steps for obtaining the API keys are included in this guide as well.</p>
<p style = 'font-size:16px;font-family:Arial;'>The OpenAI API is a powerful that enables developers to integrate the capabilities of the OpenAI language models into their own applications, products, or services. The OpenAI API allows you to leverage the state-of-the-art natural language processing capabilities of the GPT-3.5 language model, enabling you to create a wide range of intelligent and interactive experiences.
</p>
<p style = 'font-size:16px;font-family:Arial;'>By accessing the OpenAI API, you gain the ability to generate human-like text, answer questions, create conversational agents, perform language translation, assist in writing code, draft emails, write articles, and much more. The API provides a straightforward interface for making requests and receiving responses from the language model, making it easy to incorporate its advanced language capabilities into your own projects.</p>

</div>

<div class="cell markdown">

<center><img src="images/openai_header.png" alt="Generative_QA_architecture" style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=800 height=500/></center>

</div>

<br>
<div class="cell markdown">
<p style = 'font-size:20px;font-family:Arial;'><b>How to Setup OpenAI account and get the API Key</b></p>
<p style = 'font-size:16px;font-family:Arial;'><b>Steps to setup the account:</b></p>
<ul style = 'font-size:16px;font-family:Arial;'>
<li>Go to the OpenAI website: <a href="https://beta.OpenAI.com/signup">OpenAI.com</a>.</li>
<li>Click on the "Sign up" button.</li>
<li>Enter your email address and password.</li>
<li>Click on the "Create account" button.</li>
<li>You will be sent a verification email. Open the email and click on the verification link.</li>
<li>Once your account is verified, you will be logged in, you will see below screen</li>
</ul>

</div>

<div class="cell markdown">
<br>
<center><img src="images/img1.png" alt="Generative_QA_architecture" style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;"  width=800 height=800/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Click on API and you will see all the OpenAI offered services. Click on profile icon in the top right corner</li>
<br>
<center><img src="images/img2.png" alt="Generative_QA_architecture"  style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=800 height=800/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Click on View API keys. There will be one default key</li>
<br>
<center><img src="images/img3.png" alt="Generative_QA_architecture"  style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=800 height=500/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Now, you have to setup paid account first, Click on Billing to setup paid account.</li>
<br>
<center><img src="images/img4.png" alt="Generative_QA_architecture"  style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=800 height=800/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Choose the option: Select Individual if want to use for personal purposes else select second option. </li>
<br>
<center><img src="images/img5.png" alt="Generative_QA_architecture" style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=800 height=800/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Fill out the personal and billing details.</li>
<br>
<center><img src="images/img6.png" alt="Generative_QA_architecture"  style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=500 height=800/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Now, Click on Create new secret key to generate the new key.</li>
<br>
<center><img src="images/img7.png" alt="Generative_QA_architecture" style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=800 height=800/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Optional: Specify the key name.</li>
<br>
<center><img src="images/img8.png" alt="Generative_QA_architecture"  style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;" width=800 height=800/></center>
<br>
</div>

<div class="cell markdown">

<ul style = 'font-size:16px;font-family:Arial;'>
<li>Please save this secret key somewhere safe and accessible. For security reasons, you won't be able to view it again through your OpenAI account. If you lose this secret key, you'll need to generate a new one. This is the last step. You can use this key to run generative AI demos.</li>
<br>
<center><img src="images/img9.png" alt="Generative_QA_architecture"  style="border: 2px solid #ccc; border-radius: 5px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); padding: 10px;"width=800 height=800/></center>
<br>
</div>

<div class="cell markdown">

<center><h2>Thank you</h2></center>

</div>

<div class="cell markdown">

<footer style="padding-bottom:35px; background:#f9f9f9; border-bottom:3px solid">
    <div style="float:left;margin-top:14px">ClearScape Analytics™</div>
    <div style="float:right;">
        <div style="float:left; margin-top:14px">
            Copyright © Teradata Corporation - 2023. All Rights Reserved
        </div>
    </div>
</footer>

</div>
