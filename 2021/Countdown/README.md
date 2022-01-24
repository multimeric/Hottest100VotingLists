# Countdown Readme
* Scraped from: <https://www.abc.net.au/triplej/hottest100/21/1-100> and <https://www.abc.net.au/triplej/hottest100/21/101-200>
* Run the following code in the JS console on each page:
	```js
	JSON.stringify(
		Array.from(document.querySelectorAll('li[data-component=ListItem] ._1nght')).map((x, i) => {
			let split = x.innerText.split('\n');
			return {artist: split[1], track: split[0], position: i + 1}
		})
	)
	```
* Paste the JSON into a file and reformat it
