## DOM (Document Object Model)

Document Object Model (DOM) is a programming interface for HTML and XML documents.

It represents the page so that programs can change the document structure, style, and content.
The DOM represents the document as nodes and objects.

### What is Node?

- Everything in a real DOM is a node.
- The document itself is the main node -document node.
- All HTML elements are element nodes.
- All HTML attributes are attribute nodes.
- Text inside HTML elements are text nodes.
- Comments are comment nodes.

### React: The Virtual DOM

In React, for every DOM object, there is a corresponding "virtual DOM object".

A virtual DOM object is are presentation of a DOM object, like a light-weight copy.
A virtual DOM object has the same properties as a real DOM object, but it lacks the real thing's power to directly change what's on the screen.

#### How this helps:
