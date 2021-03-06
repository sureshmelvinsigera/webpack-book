-# Conclusion

As this book has demonstrated, webpack is a versatile tool. To make it easier to recap the content and techniques, go through the checklists below.

## General checklist

- **Source maps** allow you to debug your code in the browser during development. They can also give better quality stack traces during production usage if you capture the output. The _Source Maps_ chapter delves into the topic.
- To keep your builds fast, consider optimizing. The _Performance_ chapter discusses a variety of strategies you can use to achieve this.
- To keep your configuration maintainable, consider composing it. As webpack configuration is JavaScript code, it can be arranged in many ways. The _Composing Configuration_ chapter discusses the topic.
- The way webpack consumes packages can be customized. The _Consuming Packages_ chapter covers specific techniques related to this.
- Sometimes you have to extend webpack. The _Extending with Loaders_ and _Extending with Plugins_ chapters show how to achieve this. You can also work on top of webpack's configuration definition and implement an abstraction of your own for it to suit your purposes.

## Development checklist

- To get most out of webpack during development, use **webpack-plugin-serve** (WPS) or **webpack-dev-server** (WDS). You can also find middlewares which you can attach to your Node server during development. The _Development Server_ chapter covers both in greater detail.
- Webpack implements **Hot Module Replacement** (HMR). It allows you to replace modules without forcing a browser refresh while your application is running. The _Hot Module Replacement_ appendix covers the topic in detail.
- Consider using _Module Federation_ when a project gains complexity and it's using multiple different technologies or it has multiple teams working on various functionalities. The approach takes microservices to frontend development and allows you to align your frontend with microbackends.

## Production checklist

### Styling

- Webpack inlines style definitions to JavaScript by default. To avoid this, separate CSS to a file of its own using `MiniCssExtractPlugin` or an equivalent solution. The _Separating CSS_ chapter covers how to achieve this.
- To decrease the number of CSS rules to write, consider **autoprefixing** your rules. The _Autoprefixing_ chapter shows how to do this.
- Unused CSS rules can be eliminated based on static analysis. The _Eliminating Unused CSS_ chapter explains the basic idea of this technique.

### Assets

- When loading images through webpack, optimize them, so the users have less to download. The _Loading Images_ chapter shows how to do this.
- Load only the fonts you need based on the browsers you have to support. The _Loading Fonts_ chapter discusses the topic.
- Minify your source files to make sure the browser to decrease the payload the client has to download. The _Minifying_ chapter shows how to achieve this.

### Caching

- To benefit from client caching, split a vendor bundle out of your application. This way the client has less to download in the ideal case. The _Bundle Splitting_ chapter discusses the topic. The _Adding Hashes to Filenames_ chapter shows how to achieve cache invalidation on top of that.
- Use webpack's **code splitting** functionality to load code on demand. The technique is handy if you don't need all the code at once and instead can push it behind a logical trigger such as clicking a user interface element. The _Code Splitting_ chapter covers the technique in detail. The _Dynamic Loading_ chapter shows how to handle more advanced scenarios.
- Add hashes to filenames as covered in the _Adding Hashes to Filenames_ chapter to benefit from caching and separate a runtime to improve the solution further as discussed in the _Separating a Runtime_ chapter.

### Optimization

- Use ES2015 module definition to leverage **tree shaking**. It allows webpack to eliminate unused code paths through static analysis. See the _Tree Shaking_ chapter for the idea.
- Set application-specific environment variables to compile it production mode. You can implement feature flags this way. See the _Environment Variables_ chapter to recap the technique.
- Analyze build statistics to learn what to improve. The _Build Analysis_ chapter shows how to do this against multiple available tools.
- Push a part of the computation to web workers. The _Web Workers_ chapter covers how to achieve this.

### Output

- Clean up and attach information about the build to the result. The _Tidying Up_ chapter shows how to do this.

## Conclusion

Webpack allows you to use a lot of different techniques to splice up your build. It supports multiple output formats as discussed in the _Output_ part of the book. Despite its name, it's not only for the web. That's where most people use it, but the tool does far more than that.
