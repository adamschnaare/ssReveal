# ssReveal
A RevealJS-based announcements/events reader for SquareSpace feeds

## Installation
1. Copy [ssReveal-footer.html](https://raw.githubusercontent.com/adamschnaare/ssReveal/master/dist/ssReveal-footer.html) and paste it into SquareSpace's footer for your site. At your SquareSpace account, navigate to `Settings > Advanced > Code Injection`, and paste this code into the **Footer section**.
2. Create a page on your SquareSpace account for your slideshow. I'd recommend making it an unlinked page.
3. On that page (2), click `Settings > Advanced` and paste [ssReveal-header.html](https://raw.githubusercontent.com/adamschnaare/ssReveal/master/dist/ssReveal-header.html) into the **header** section. Note...after you do this, the only way to edit your page settings will be from the left-hand admin panel, as the script installed on the page deletes everything on the page.
4. In that section, edit the config section (the very top, shown below), pasting in **your correct Urls**. See Configuration section for details
5. It's also important to set your location/time correctly with SquareSpace. Do so in their settings area.

```
// Config
var ssReveal = {
    config: {
        baseUrl: 'https://themill.church',
        feedUrl: 'https://themill.church/events/?format=json-pretty',
        range: 'upcoming', // past,upcoming
        linkText: 'See Details'
    }
};
```

## Configuration
`baseUrl`: Your website url up to the `.com`, or whatever. Be sure it starts with `https` not `http`
`feedUrl`: Your events feed url. Add `?format=json-pretty` to the end. Be sure it starts with `https` not `http`
`range`: whether you want `past` or `upcoming` events
`linkText`: the text that shows up on the links back to the actual event pages

## Usage
- Once setup, just navigate to your create page url, and you're good to go!
- Repeat for each events feed you want to use as an announcements slideshow

## Manual Export
There is also a manual export file, which when run on a webserver locally will print HTML formatted for an email of the upcoming events.
