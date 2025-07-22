# Plan for Integrating nikol.AI Chatbot into Portfolio Website

## Overview
This plan outlines the development and integration of a custom chatbot, `nikol.AI`, into my personal portfolio website. The chatbot will serve as a digital assistant, providing information about my CV, projects, diplomas, About Me (volunteering, photo projects, teaching, IT, martial arts), and contact details, enhancing user engagement. The project will leverage an n8n workflow with Mistral's API for backend processing. The website will support multiple languages—Russian (default), English, and Chinese—to target job opportunities in Russia while remaining accessible in China and globally. Retro styling (CRT, Windows 98, Matrix effect) and animations inspired by https://anulikajoy.com/ will be implemented after language functionality is complete.

## Website Structure
- **Home**: Central chat interface with `nikol.AI`, showcasing an overview and navigation.
- **CV**: Detailed resume with work experience, education, and skills.
- **Projects**: Portfolio of technical projects.
- **Diplomas**: Display of diplomas and certifications.
- **About Me**: Showcase of personality, including volunteering projects, photo projects, teaching, IT achievements, and martial arts success.
- **Contact**: Contact form and details.

## Phases

### Phase 1: Project Setup with Multilingual Support
- **Status**: In Progress
- **Tasks**:
  - Set up the project structure with updated HTML/CSS files (`index.html`, `cv.html`, `projects.html`, `certificates.html`, `about-me.html`, `contact.html`, `style.css`).
  - Implement a language switch button in the navbar with flag icons (Russian, English, Chinese) using SVG files from https://flagicons.lipis.dev/.
  - Translate placeholder content into Russian and Chinese, with English as an option.
  - Use JavaScript to dynamically switch languages, storing the preference in `localStorage`.
- **Notes**: Language switch with SVG flags is implemented on all pages; "Дипломы" replaces "Сертификаты" in the structure.

### Phase 2: Chatbot UI Integration
- **Status**: Not Started
- **Tasks**:
  - Design a central chat interface for the home page (`index.html`), making it the primary focus.
  - Add a toggleable chat widget to other pages (`cv.html`, `projects.html`, `certificates.html`, `about-me.html`, `contact.html`).
  - Include multilingual support for chat messages.
  - Implement isolated `homeChatHistory` for the home page, with fresh chat widgets on other pages.
- **Notes**: Chatbot UI will follow language implementation across all pages.

### Phase 3: Chatbot Backend Prototype
- **Status**: Not Started
- **Tasks**:
  - Set up an n8n workflow with a Webhook node to receive user input.
  - Integrate Mistral's API via n8n's HTTP Request node or Mistral-specific node for natural language processing, supporting multilingual responses.
  - Update JavaScript in all HTML files to send user messages to the n8n webhook and display Mistral responses.
- **Notes**: Backend integration is pending the provision of the n8n webhook URL or Mistral API details.

### Phase 4: Content Staging
- **Status**: Not Started
- **Tasks**:
  - Create a `knowledge-base.md` file summarizing content from `cv.html`, `projects.html`, `certificates.html`, `about-me.html`, and a bio, with translations in Russian, English, and Chinese.
  - Feed the knowledge base into Mistral via n8n to enable contextual, multilingual responses.
- **Notes**: Content staging will occur after real data is provided.

### Phase 5: Retro Styling and Refinement
- **Status**: Not Started
- **Tasks**:
  - Apply retro styling inspired by https://anulikajoy.com/, including:
    - Matrix rain effect with green characters.
    - CRT scanline overlay.
    - Vintage Windows 98-inspired cursor animations.
  - Use prompt engineering to make `nikol.AI`’s tone friendly, witty, and retro-inspired.
  - Implement fallback responses with a retro twist.
  - Replace the CSS-based `.chat-logo` with a retro-styled image.
- **Notes**: Retro styling is deferred until language and core functionality are stable.

### Phase 6: Launch and Documentation
- **Status**: Not Started
- **Tasks**:
  - Merge the multilingual chatbot into the live portfolio website.
  - Write a blog post or case study about building `nikol.AI`, detailing the multilingual design process and outcomes.
- **Notes**: Launch will make the chatbot publicly accessible, with documentation highlighting the multilingual feature.

## Current Status (as of July 22, 2025, 04:05 AM EDT)
- Phase 1 is in progress, with multilingual support and SVG flag implementation on all pages; "Дипломы" replaces "Сертификаты".
- Phases 2-6 are pending further development.
- The home page chat interface is isolated with `homeChatHistory`, and other pages feature fresh chat widgets.

## Next Steps
- Confirm the exact subfolder name (e.g., `svg/`, `1x1/`, `4x3/`) from the unzipped flagicons folder to adjust flag paths if needed.
- Provide the n8n webhook URL or Mistral API details to proceed with Phase 3.
- Revert to the current bland style temporarily if retro styling hurdles arise.