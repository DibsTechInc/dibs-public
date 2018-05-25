# Instructions to integrate your website with the Dibs widget

### 1. Installing widget code:

Please add this snippet of code to the `<head>` of your site on the pages you want the widget to display:
```
<script src=“https://d1yzs2hnv2a9ej.cloudfront.net/dibsloader.js?id=90“> </script>
```
### 2. Updating links:

In order to seamlessly integrate into our clients' sites, our widget listens for click events
on HTML tags that have certain HTML5 dataset attributes* which indicate our widget should open
to our schedule or other specified pages. Any HTML tag on the studio's site that will interact
with our widget must have the following attribute:

`data-dibs="true"`

In addition to this first attribute, any HTML tag with the following attributes can interact with the widget:

- `data-dibs="true"` - any tag with this attribute with just this attribute alone will open the Dibs widget to the class schedule.

- `data-dibs-pricing="true"` - any tag with this attribute will open the widget to the page where users can buy packages and memberships to the studio.

- `data-dibs-profile="true"` - any tag with this attribute will open the widget to the user's personal setting page

- `data-dibs-account="true"` - any tag with this attribute will open the widget to the user's account page with links to where they may view active plans, upcoming classes, and adjust their account settings.

- `data-dibs-signup="true"` - any tag with this attribute will open the widget to the sign up page

- `data-dibs-login="true"` - any tag with this attribute will open the widget to the login page
For example, an HTML div tag on your site like the following:

```
<button data-dibs="true"> See classes </button>
```

will open the widget to the schedule page without any other action required (provided the widget script is installed). The following tag:

```
<button data-dibs="true" data-dibs-signup="true"> Sign up </button>
```

will open the widget to the signup page for new users.

Please reach out to us if you have any questions, happy coding!

*: You can learn more about HTML5 dataset attributes here:

[MDN: HTML Dataset Attributes](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset)

[MDN: How to use dataset attributes](https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes)

