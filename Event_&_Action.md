# Events and Actions

## Use

Most UI elements (e.g. the Button UI element) can react to a user's interaction (e.g. clicking on the corresponding pushbutton). This reaction can trigger a handling method to be called within the view controller.

Events are used to communicate between controllers and enable one controller to trigger event handlers in a different controller. Cross-component communication can be implemented using the interface controller's events. Events that were created in the component controller are visible within the component only.

## Action
Actions are runtime objects that associate a client-side event with a server-side response. When you create an action object, the system automatically creates an action handler method. You link the event, the UI element is equipped with, with the appropriate action object.

If a UI element has been inserted several times into a view, you can equip their events with different actions as necessary. The event is then processed by the corresponding event handler depending on the action that is linked.

Actions can also be reused within a view. This means that an action can be linked to the events of several (or even different) UI elements. In this manner, it is possible to write a single, generic action event handler method that can respond to a variety of events raised by multiple UI elements.

## Note
A view controller should be written such that it is only ever a consumer of data, never a generator. This means that view controllers should never contain coding to interact with a back end system.

## Recommended Action Architecture:

  - Once control has been passed to the action event handler method in the view controller, this method should delegate all interaction with the back-end system to a non-visual controller.

  - Hence the call to a method happens to live in the component controller. This method then interacts with the back-end system via the model object.

  - The data returned from the model object is passed from the component controller to the view controller through the technique of context mapping.

## Inbound Plug Events

Inbound plugs in a view also react like an event. Therefore, when a view is called using an inbound plug, the event handler that is optionally available for the inbound plug is always called first. In this case event handling takes place within the current view controller, however.

The same applies for the inbound plugs of an interface view. In the corresponding window controller, an event handler is created. It can then be programmed further, as appropriate.

## Here is a list of the most commonly used DOM events, just for reference:

## Mouse events:

  - `click` - occurs when an element is clicked with the left mouse button (on devices with touch screens, it occurs on touch).
  - `contextmenu` - occurs when an element is right-clicked.
  - `mouseover / mouseout` - when the mouse moves over / leaves the element.
  - `mousedown / mouseup` - when the mouse button was pressed / released on the element.
  - `mousemove` - when moving the mouse.

## Events on controls:

  - `submit` - The user has submitted the form .
  - `focus` - The user focuses on the element, such as clicking on an .

## Keyboard events:

  - `keydown and keyup` - when the user presses/releases a key.

## Document events:

  - `DOMContentLoaded` - When the HTML is loaded and rendered, the DOM of the document is fully built and available.

## CSS events:

  - `transitionend` - when the CSS animation is complete.

## Event handlers

An event can be assigned a handler, that is, a function that will work as soon as the event occurs.

A user performs actions like pressing buttons or making selections in dialogs. These actions are sometimes turned into events by the framework. Events are like messages sent to methods that have registered to be notified for a specific event type. The term "event" is also used for specific types, such as the "Change" event or "Submit" event of an edit box. The user doesn't directly submit a message; instead, actions on UI elements may result in the framework detecting events. The framework then finds which methods are registered for these events and invokes them with the proper arguments. This model allows the application to handle specific logic for events without needing to track every system or user move—the framework takes care of this and notifies relevant event handlers when needed.
