# Keyboard Text Tool

 **language: [English](README.md), [中文](README_zh.md)**

# **Project Overview**
This project, based on the Vue framework and using HTML, CSS, and JavaScript technologies, creates a keyboard key visualization interface. It can accurately display the pressed and released states of keyboard keys in real-time and also show the corresponding key codes. When a user operates the physical keyboard, the corresponding keys on the interface will change color dynamically to reflect the state change.

# **Function Features**
- **Instant Response Feedback**: Efficiently captures the keyboard press (keydown) and release (keyup) events and makes corresponding display changes on the visualization interface promptly without delay or lag, providing a smooth interaction experience for the user.
- **Precise State Identification**:
    - When a key is pressed, its background color immediately changes to `#a0a0a0` and is clearly labeled as "Pressed" on the interface, allowing the user to intuitively know the key state.
    - After the key is released, the background color smoothly transitions to `#888888` and is shown as "Nerver", clearly distinguishing different operation stages.
    - For special keys such as function keys (F1 - F12) and arrow keys, when pressed, it not only updates the interface display accurately but also intelligently blocks their default behaviors, such as effectively preventing the F5 key from refreshing the page and other unnecessary operation interferences.
- **Convenient Key Code Display**: The key code of the currently pressed key will be prominently displayed in a specific area of the interface, which provides great convenience for developers during debugging, enabling them to quickly locate and analyze problems.

# **Project Structure**
- **`template`**: This part contains carefully written HTML code used to construct the overall layout of the keyboard visualization interface. It comprehensively covers the detailed definitions of key elements in different functional areas such as the main keyboard area, function key area, numeric keypad area, and status display area. And each key is cleverly assigned a unique `id` attribute so that various operations and state updates can be precisely performed in the JavaScript code.
- **`script`**: Mainly contains the JavaScript code logic in the Vue component. In the `mounted` lifecycle hook function, listeners for keyboard press and release events are added skillfully. The `keydown` function is responsible for handling key press events. It accurately judges whether the key belongs to a special type that requires special handling based on the `keyCode`. If the corresponding key element exists in the interface, it will methodically change its background color and update the `keycode` data in a timely manner. The `keyup` function is used to handle key release events. Its operation process is similar to that of the press event. It will smoothly change the key background color and reset the `keycode` data to `null`, ensuring that the interface state always remains consistent with the actual keyboard operation.
- **`style`**: The style code written in Less defines the styles of various keys comprehensively, including but not limited to precise size settings, delicate color combinations, skillful shadow creations, and elegant border radius treatments. It also sets the display styles of keys in different states carefully. In addition, it makes overall planning for the layout and style of the entire interface, such as the reasonable arrangement of each keyboard area, appropriate width settings, and harmonious background color determination, aiming to create a beautiful and easy-to-use visualization interface.

# **Usage Guide**
1. **Clone the Project Locally**:
git clone https://github.com/tsrdzy/KeyboardTextTool

2. **Launch the Project Interface**: Enter the project directory in the terminal and run the `npm run serve` command to start the project. Then enter the corresponding address (usually `http://localhost:8080`) in the browser to open the `index.html` page, and the exquisite keyboard visualization interface will be presented.
3. **Perform Interaction Operations**: In the opened interface, when the user presses or releases a key on the physical keyboard, the corresponding key on the interface will change color immediately. At the same time, the key code of the currently pressed key will be displayed synchronously at the bottom of the interface, facilitating the user to observe and understand the operation feedback in real-time.

# **Attention Points**
- This project focuses on demonstrating the visualization effect of keyboard keys and basic event handling mechanisms. In the face of some extremely complex keyboard layouts or special key combination scenarios, there may be certain compatibility issues. If there are further requirements, in-depth optimization and expansion work can be carried out to improve the robustness and applicability of the project.
- The styles and layout in the project are carefully implemented based on specific design requirements and user experience goals. If you want to apply it to other projects, comprehensive and detailed adjustments may be required, including but not limited to style adaptation, layout reconstruction, and function expansion and optimization, to ensure a perfect integration with the new project environment and requirements.
