# Alt Decision Tree For Umbraco Developers

This decision tree describes how Umbraco developers should use the `alt` attribute of the `<img>` element in various situations.

## Key Rules Before You Begin

**1. Avoid Using Alt Text Fields in the Umbraco Media Library**
Alt text should not be added as a field for images directly in the Media section. The context in which the image is used will determine if alt text is necessary, and therefore alt text fields should be placed where users are adding content.

**2. If No Alt Text is Provided**
If the user does not provide alt text for an image, the image should have an empty `alt` attribute, so that it can be ignored by assistive technologies. Example: `<img src="image.jpg" alt="" />`.

---

## How to Use Alt Text

### Is the image likely to contain text?

* **No:** Continue
* **Yes:** Provide an alt text field explaining to users that they should provide the text of the image unless the image is purely decorative.

### Is the image used in a link or a button?

* **No:** Continue
* **Yes:** Provide an alt text field explaining to users that they should communicate the destination of the link or action taken.

### Will the image provide meaning or context to the content of the page?

* **No:** Continue
* **Yes:** Provide an alt text field explaining to users what good alt text looks like.

### Is the image purely decorative or not intended for users?

* **No:** Continue
* **Yes:** Don't have an alt text field, but do output an empty `alt` attribute on the `<img>` element. e.g. `<img src="decorative-image.jpg" alt="" />`

### If the image doesn’t fit into any of these categories:

Don’t worry! For additional guidance on how to determine whether an image needs alt text, refer to the [W3C Web Accessibility Initiative (WAI) website](https://www.w3.org/WAI/tutorials/images/).
