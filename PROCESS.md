# Process Journal

## 1. Initial Concept & Ideation
- **Inspiration**: I wanted to create an interactive web application that merges aesthetic visual appeal with lightweight psychological feedback for everyday life.
- **Core Interaction Loop**:
  - *Input*: The user enters from the cover page and clicks to select a single card from the 78 laid-out cards using their intuition.
  - *Response*: The program captures the click coordinate, triggers a 3D card-flip animation, and randomly pulls a corresponding card from the database.
  - *Feedback*: Highlights the selected card, dims the rest, and dynamically displays the personalized fortune interpretation and reset button below.

## 2. Design & Code Iterations
- **Layout Challenge**: Initially, I considered a standard grid layout, but it looked cluttered and lacked a sense of ritual. By dynamically calculating rotation angles and transform origins using math logic, I successfully implemented a clean, arc-shaped fan layout.
- **Error Handling & Edge Cases**:
  - To prevent accidental "double clicks" or multiple selections, I introduced a state flag. Once a card is drawn, all remaining unselected cards have their pointer events disabled, preventing interaction errors.
  - For the reset flow, I refined the function so it not only clears the previous flipped state smoothly but also allows users to return to the cover view and reshuffle effortlessly.

## 3. User Trial & Iteration
- **Testing Process**: I invited my roommate to test the web application without providing prior instructions to see how intuitively they could navigate the interface.
- **Observations & Issues Identified**: 
  - **Usability**: The roommate felt slightly overwhelmed by the dense array of 78 cards upon entering the main screen, and after drawing a card, they were initially unsure how to start a new round.
  - **Logic/Data Bug**: During testing, we noticed that whenever a Minor Arcana card was drawn from the deck, the generated interpretation text remained identical across different cards, failing to provide unique feedback for individual Minor Arcana elements.
- **Improvements & Debugging Made**:
  - **Fixed Minor Arcana Interpretations**: Resolved the database logic issue so that each suit and rank in the Minor Arcana dynamically displays its corresponding unique card meaning and element guidance.
  - **Enhanced Guidance**: Added a prominent, friendly prompt box at the top of the main page to direct user attention.
  - **Added Reset Option**: Introduced a bright yellow "Return to Cover · Reset" button below the result container, allowing users to effortlessly reshuffle and restart the divination experience.

## 4. AI Tool Usage
- **Adopted Suggestions**:
  - **ChatGPT** use it to generate the initial background imagery (`background.png`) and the tarot cover art (`cover.png`) to establish the visual aesthetic.
  - **Gemini** use it in an iterative process to repeatedly debug and refine the frontend code, optimizing the CSS 3D card-flip matrix and ensuring smooth interactions across the 78-card fan layout.

## 5. Credits & Development History
- Maintained a consistent and meaningful Git commit history throughout the development process, recording key feature updates in accordance with course guidelines.