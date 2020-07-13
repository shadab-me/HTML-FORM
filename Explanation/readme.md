## BLOCK-readText

### Building HTML Forms

Forms are an essential part of websites, as they provide a way to collect the user's information. For example, during user registration, you would like to collect information like name, email address, password, billing information, etc. A form collects different information and then process it with the backend application based on the logic.

In this lesson, we are going to look at how forms are initialize using HTML, and then we will learn to style it using CSS. We will see what are the different form elements used to collect the data from the users. Although there are a lot of things behind the scene while processing the data in the backend, we won't that much deeper. We will stick to the basics only.

#### The `<form>` Element

To initialize a form inside the HTML document `<form>` element is used. A form element is a block-level element much like a div that can wrap all the essential elements required within the form.

```
  <form action="/login" method="post">
    <!-- Form elements like input, textarea etc. -->
  </form>
```

The `form` elements come with a few handfuls of attributes like `action` and `method`. The `action` attribute contains a URL to which the collected information from the form will send for further processing by the server. The `method` attribute contains HTTP methods that the browser uses to submit the data.

Both of these attributes are essential for the processing and submitting the form data. Although, being a front-end developer you don't have to worry about all these, but don't forget to add these attributes so that for back-end developer it will be helpful for further processing.

There are various elements that a form element can wrap to collect the user's data. For example, input, textarea, checkbox, radio button, etc.

#### Text and Textarea Fields

When it comes to collecting the text-based data there are a few different elements. For single-line input, the `input` elements are used and for multi-line `textarea` element is used.

**Text Fields**

The `input` fields are one of the primary elements of the form to collect the single-line text-based information from the users. For example, if we want to collect the user's name, email, password, or any search query, etc.

Based on what type of information is to be collected within the control the `input` field comes with `type` attribute. One of the most popular values for the `type` attribute is `text` mostly used to collect the user's name.

```
  <input type="text" name="username">
```

The `input` element is a self-contained `inline-level` element that cannot wrap any other content inside it.

Apart from the `type` attribute input field should also have a `name` attribute used as the name of the control. The `name` attribute is also essential while processing the data in the backend application.

Let's see a few more examples of the `type` attribute.

```
  <input type="email" name="email-address">
  <input type="password" name="password">
  <input type="search" name="search">
  <input type="date" name="birthday">
  <input type="time" name="session-time">
  <input type="number" name="cost">
```

These are the few examples of a type of attribute value that you usually see within the `input` element. Apart from these, there is a list of input types that may find on a page.

- color
- date
- datetime
- email
- month
- number
- range
- search
- tel
- time
- URL
- week

**Textarea Field**

Whenever we need multi-line text-based information from users the `textarea` element is used. For example for any messages or any query related information.

```
  <textarea name="message" col="30" rows="10">
    Your Message...
  </textarea>
```

The `textarea` element doesn't accept the `type` attribute because there is just one type. But the `name` attribute is needed.

The textarea element accepts the other two attribute `col` and `rows` that size of the textarea element. The `col` attribute is the width in terms of characters and the `row` attribute is height in terms of several lines.

#### The Radio Button and Checkbox Control

The `radio` button and `checkbox` within the HTML form allow users to select data using multiple choices. It can bethink as multiple-choice questions.

**The Radio Button**

The radio buttons are used when users need to select one option out of multiple options.

Radio buttons are created using the input element with a `type` attribute value of `radio`.

```
  <input type="radio" name="language" value="HTML" checked> HTML
  <input type="radio" name="language" value="CSS"> CSS
  <input type="radio" name="language" value="JavaScript"> JavaScript

```

All the radio button `type` attributes must have the same value so that they will be within a group correspond to one another.

Opposite to text-based input, all the radio button accepts the `value` attribute to set the specific value for each `input` element. In text-based input, the value is determined by the user's input, but on the radio, button users are making a multiple-choice option not providing the values of the `input` element.

There is `checked` boolean attribute to preselect any option.

**The Checkbox Control**

Using radio button input a user can select one option out of multiple options. But many times there can a need of selecting multiple options.

To provide the ability to select multiple options `input` element is used with `type` attribute value of `checkbox`.

```
  <input type="checkbox" name="language" value="HTML" checked> HTML
  <input type="checkbox" name="language" value="CSS"> CSS
  <input type="checkbox" name="language" value="JavaScript"> JavaScript
```

The rest of the attribute value remains the same similar to the radio button.

#### Drop Drown Lists

When it comes to providing a long list of options to the users, the radio button or checkbox may not be a good experience. Let's say the user has to select one option out of ten multiple options, showing ten multiple options can daunting especially on mobile view. A drop-down list would be a perfect way for a long list of options.

The HTML provide `<select>` element to create drop-down list. The `<select>` elements wraps `<option>` elements to markup all the option within the list.

```
  <select name="language">
    <option value="HTML" selected>HTML</option>
    <option value="CSS">CSS</option>
    <option value="JavaScript">JavaScript</option>
    <option value="Ruby" selected>Ruby</option>
    <option value="Python">Python</option>
    <option value="PHP">PHP</option>
  </select>
```

The `option` elements come with the `value` attribute which corresponds to the `name` attribute on the `select` element. All the visible content will reside inside the `option` element, based on which user will select the option.

If an option you would like to show the user preselected, much like `checked` boolean attribute you can apply `selected` boolean attribute on the option element.

> **Multiple Selections**
>
> Applying `multiple` boolean attribute provide ability to users to select multiple options from a drop-down list.
> To select multiple options the user will have hold the Shift key while clicking the options.
>
> ```
>  <select name="language" multiple>
>    <option value="HTML" selected>HTML</option>
>    <option value="CSS">CSS</option>
>    <option value="JavaScript" selected>JavaScript</option>
>    <option value="Ruby" selected>Ruby</option>
>    <option value="Python">Python</option>
>    <option value="PHP">PHP</option>
>  </select>
> ```
>
> Using selectd boolean attribute on more than one options will show the user preselected multiple options.

#### Other Inputs

Besides all the `input` elements that we have seen above, there are a few other types of input elements, like `hidden` input and `file` input. These inputs are helpful during form processing.

**Hidden Input**

The hidden type of input is created using the `hidden` value for the `type` attribute within an input element.

```
  <input type="hidden" name="tracking-code" value="abc-123">
```

The `hidden` inputs are typically used to track-codes or other pieces of information which are not relevant to users, but helpful in processing the form data. The hidden inputs are not displayed on the page but can be found while viewing the source code of the page.

**File Input**

The `file` input allows users to add files to a form. To create file input use file value for the type attribute within an input element.

```
  <input type="file" name="file">
```

#### Buttons

Once the required information is filled up by the users, the form needs to be submitted for further processing. To submit form data submit button is created. Most commonly the submit buttons are created using `<input>` or `<button>` elements.

**Submit Input Button**

To create the input button use `submit` value for the `type` attribute within the input element.

```
  <input type="submit" name="submit" value="send">
```

**Submit Button Element**

As an `<input>` is a self-contained element cannot wrap any other content, so there is `<button>` element in HTML to submit the form data.

```
  <button name="submit">
    <strong>Send</strong> Message
  </button>
```

The `button` element provides more control over the style of the `input` element. The `button` element comes with an opening and closing tag that may wrap other elements. Sometime you may wrap an icon inside the `button` element, for better style and design of the button.

#### Organizing Form Elements

When working with the form, knowing how to collect user's data using different elements like `input`, `textarea`, `select`, `button` etc is just half of the battle. The most challenging part is to organize those individual elements inside the form. The user must need to understand what is being asked to them while interacting with the form.

To organize and design a form with better user experience HTML provides a few extra elements like label, legend, and fieldset. These elements guide users while entering the form.

**The `<label>` element**

The `<label>` tag inside the form elements works as a label or heading for any form elements. The `label` is and inline-level element that guide the users what type of information has to be entered in the input or controls. For example:

```
  <label for="username">Username</label>
  <input type="text" name="username" id="username">
```

The `label` element may include `for` attribute The value of the attribute must be the same as the `id` attribute value on the form element. Keeping the `for` attribute and `id` attribute value tie them together. That allows users to click on the `label` and bring focus on the connected form element.

Sometime `label` element may wrap the input element with a type of radio or checkbox, doing so you can omit the for and id attribute.

```
  <label>
    <input type="radio" name="language" value="HTML" checked> HTML
  </label>
  <label>
    <input type="radio" name="language" value="CSS"> CSS
  </label>
  <label>
    <input type="radio" name="language" value="JavaScript"> JavaScript
  </label>
```

**The `<fieldset>` element**

Much like `<section>`, `<fieldset>` is a block-level element. It allows us to group the different form controls and labels into organized sections.

```
  <fieldset>
    <label>
      Username
      <input type="text" name="username">
    </label>
    <label>
      Password
      <input type="password" name="password">
    </label>
  </fieldset>
```

The `<fieldset>` element by default comes with a border outline that may be modified using CSS.

**The `<legend>` element**

The `<legend>` element used to provide a caption or heading to a form. That helps users to understand what type of is.

```
  <fieldset>
    <legend>Login</legend>
    <label>
      Username
      <input type="text" name="username">
    </label>
    <label>
      Password
      <input type="password" name="password">
    </label>
  </fieldset>
```

#### Additional Attributes

In addition to all the attributes that we have seen above, there are other attributes also with different functionality. For example, disabling any input and adding other form validations.

**The Disable Attribute**

There comes a `disabled` boolean attribute that turns off any form of control.

```html
<label>
  Username
  <input type="text" name="username" disabled />
</label>
```

Doing so the users won't be able to interact with the elements, but it will display on the page. The `disabled` element won't send any information to the server for the form processing.

**The Placeholder Attribute**

The `placeholder` attribute provides additional information on how the form input should be filled. It just works as a hint within `input` or `textarea` field for the users.

```html
<label>
  Email Address
  <input type="email" name="email-address" placeholder="xyz@example.com" />
</label>
```

The placeholder value will appear on the page inside the form control but once you focus or click on the element the `placeholder` value disappears.

**The Required Attribute**

If a form element contains `required` boolean attribute means that field must not be left blank. That field must contain a value before submitting the form to the server.

```html
<label>
  Email Address
  <input type="email" name="email-address" required />
</label>
```

If the field is left blank the form will through an error message.
