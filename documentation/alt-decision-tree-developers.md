# Alt Decision Tree For Umbraco Developers

This decision tree describes how Umbraco developers should use the `alt` attribute of the `<img>` element in various situations.

Before getting into the tree there are two main rules:

1) Please do not put alt text as a field against images in the Umbraco Media Library. Alt text on images is all about context, so if it's needed please add alt text fields where users are adding their content.

2) If no alt text is provided by the user for an image, output an empty `alt` attribute on the image, so the image can be ignored by assistive technologies.

## Will the image likely contain text?

No:
Continue

Yes:
Provide an alt text field explaining to users that they should provide the text of the image unless the image is purely decorative.

## Is the image used in a link or a button?

No:
Continue

Yes:
Provide an alt text field explaining to users that they should communicate the destination of the link or action taken.

## Will the image contribute meaning to the current page or context?

No:
Continue

Yes:
Provide an alt text field explaining to users what good alt text looks like.

## Is the image purely decorative or not intended for users?

No:
Continue

Yes:
Don't have an alt text field, but do output an empty `alt` attribute on the `<img>` element. e.g. `<img src="decorative-image.jpg alt="">`

## Your image doesn't fit any of these

Don't panic. Have a read about images on the W3C Web Accessibility Initiative (WAI) website https://www.w3.org/WAI/tutorials/images/.
