## Add an Uber button

Uber provides ready-made image [assets](https://d1a3f4spazzrp4.cloudfront.net/uberex/Uber_API_Design_Guidelines.zip) that we can use to make our Uber button. Uber also provides these helpful [design guidelines](https://developer.uber.com/v1/design-guidelines/) that offer rules of thumb for button placement and sizing.

To start, we need to create the button itself. We can accomplish that with a simple `div` inserted below the map `img`: `<div class="button"></div>`

Notice we've used a `div` for the button rather than an `img`: this is because we're planning to overlay the button with live time estimates to the nearest Uber ride!

Now let's load the Uber button image inside the `div`. 

Open up the [assets](https://d1a3f4spazzrp4.cloudfront.net/uberex/Uber_API_Design_Guidelines.zip) you downloaded from Uber and navigate to the Retina Display-ready Uber buttons (e.g. `/Users/cameron/Downloads/Uber API Design Guidelines/Assets/Uber API Buttons/Grey/PNGs/2x`) and choose the image you prefer. Copy it into the `/img` folder in the directory containing your invitation's HTML and CSS.

__Note:__ Depending on your invitation's style, you can choose either the black or grey buttons provided by Uber.

We'll link the chosen image to the div by specifying the `background-image` property in the `.button` class in CSS:

```css
.button {
		background-image: url('../img/UBER_API_Button_2x_Grey_hard edge.png');
		background-size: cover;
		width: 280px;
		height: 44px;
		margin: 0 auto;
}
```

__Note:__ Because we're using the `background-image` property, we have to specify the width and height of the `.button` class; otherwise, the `div` won't appear on our invitation.