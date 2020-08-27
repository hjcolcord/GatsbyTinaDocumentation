# Adding TinaCMS to a Gatsby Project

Tina provides a way to edit content directly within the webpage of a "gatsby develop" session. The following instructions will
explain how to add the tool to a gatsby project, as well as how to begin populating editable content for site pages.

## Project Instantiation

Install the Gatsby version of TinaCMS and its dependencies

```bash
yarn add gatsby-plugin-tinacms gatsby-tinacms-git gatsby-tinacms-json styled-components
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
          plugins: ['gatsby-tinacms-git', 'gatsby-tinacms-json'],
        ],
      },
    },
    // ...
  ],
}
```

## Run The Development Server
```bash
yarn install && gatsby develop
```


## Adding a Page
1. Create a "pages" subdirectory within the "src" directory of the project.
2. Create a .js file with the desired url name within "pages".
3. Add the required components to set up a basic React page. (seen below)
```javascript
import React from 'react';

// import { useStaticQuery, graphql } from "gatsby"

const Home = () => {

    return (
      <div>
        {Page Content}
      </div>
    )
};
export default Home;

```

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)