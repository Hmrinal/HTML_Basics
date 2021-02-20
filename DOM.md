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

- When you render a JSX element, every single virtual DOM object gets updated.
- This sounds incredibly inefficient, but the cost is insignificant because the virtual DOM can update so quickly.
- Once the virtual DOM has updated, then React compares the virtual DOM with a virtual DOM snapshot that was taken right before the update.
- By Comparing the new virtual DOM with a pre-update version, React figures out exactly which virtual DOM objects have changed. This process is called "diffing".
- Once React knows which virtual DOM objects have changed, then React updates those objects, and only those objects, on the real DOM. In our example from earlier, React would be smart enough to rebuild your one checked-off list-item, and leave the rest of your list alone.
