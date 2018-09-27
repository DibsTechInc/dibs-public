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

- `data-dibs-gift="true"` - any tag with this attribute will open the widget to the page where users can purchase gift cards (if you choose to have this feature).

- `data-dibs-raf="true"` - any tag with this attribute will open the widget to the Refer-A-Friend page where users can refer Dibs to your studio for bonus credit when their referral makes a purchase.

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

---

## Schedule Filtering

#### Filtering by Class

Using our data attributes, it is possible to open the Dibs schedule to a particular
class automatically. However, in order to do so, you need API access to your booking
platform (i.e. MindBody, ZingFit, etc.) in order to get the unique identifier for
each class. In MindBody, for example, this would be the class's ID field.

If you add the `data-dibs-classid="<class's ID>"` attribute, to an HTML element on
a page with the Dibs widget code, it will open the Dibs schedule to the date of the class
and filter the schedule to only show only that particular class.

#### Filtering by Location

Using our data attributes, it is also possible to open the Dibs schedule so that
it only shows classes at one of the studio's locations.

If you add the `data-dibs-filter-locations="12"` attribute to an HTML element, it will
open the schedule to the location with the Dibs location ID of 12.
Location IDs differ by studio and using the wrong location ID will result in the
schedule opening and displaying no classes at all.
In order to find out which location IDs to use for your studio, please contact Dibs and
we will provide you the IDs promptly.

If you want to filter the schedule to multiple locations, set the value of the
`data-dibs-filter-locations` attribute to be multiple location IDs separated by
a comma (no spaces).

#### Filtering by Class Name

It is also possible to filter the Dibs schedule by class name as well.

If you add the `data-dibs-filter-classname="HIIT Row"` attribute to an HTML element,
it will open the schedule and only display classes named "HIIT Row". This filter will work
with any class name your studio offers. The class name matching is case insensitive and ignores
whitespace and punctuation.

Currently, this data attribute only supports filtering the schedule to one particular class
name. If you would like to be able to use it to include multiple class types, please reach
out to Dibs.

---

Please reach out to us if you have any questions, happy coding!

*: You can learn more about HTML5 dataset attributes here:

[MDN: HTML Dataset Attributes](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset)

[MDN: How to use dataset attributes](https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes)
