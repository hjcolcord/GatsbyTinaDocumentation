# Adding TinaCMS to a Gatsby Project

Tina provides a way to edit content directly within the webpage of a "gatsby develop" session. The following instructions will
explain how to add the tool to a gatsby project, as well as how to begin populating editable content for site pages.

## Project Instantiation

Install the Gatsby version of TinaCMS and its dependencies

```bash
yarn add gatsby-plugin-tinacms styled-components
```

## Add the TinaCMS Plugin
gatsby-config.js

```javascript
module.exports = {
  // ...
  plugins: [
    {
      resolve: 'gatsby-plugin-tinacms',
      options: {
        // The CMS will be disabled on your production site
        enabled: process.env.NODE_ENV !== 'production',
        sidebar: true,
        plugins: [
          // We'll add some gatsby-tinacms plugins later
        ],
      },
    },
    // ...
  ],
}
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)