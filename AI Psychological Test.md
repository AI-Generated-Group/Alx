Our current view on the last tarot card scheme is as follows. We want to make an entertainment tool for AI psychological testing. The general logic is that I prepare a story and 20-30 characters (can we refer to the logic of tarot cards? In this part, we are thinking about how to prepare these characters and stories better). Then the user can choose several categories, such as career, love, wealth, etc., and then 10 questions will appear (for example, which angel do you choose, according to your first intuition, etc.). These pictures give users space for induction. Four pictures appear for each question. These pictures are generated based on these characters. Finally, AI interprets your choice and generates a text.

# Logical thinking of character design

**Psychological dimension**

1. **MBTI personality model**: divide characters into 4 categories (intuitive/sensing, thinking/emotional, etc.)

2. **Jungian archetype theory**: 12 basic archetypes (such as orphans, warriors, magicians, etc.)

3. **Need hierarchy theory**: corresponding to Maslow's pyramid (survival/security/social/respect/self-realization)

**Narrative dimension**

1. **Hero's journey structure**: each character represents a journey stage (departure/enlightenment/return)

2. **Conflict type**: interpersonal/self/environmental conflict

3. **Symbolic system**: natural elements (fire/water/wind/earth) + cultural symbols (such as "judgment" and "lovers" in tarot cards)

**Example:**

**Character name**: Misty Traveler

**Core archetype**: Explorer (Jungian archetype) + INTP (MBTI)

**Symbolic elements**:

- Main element: wind (change)
- Secondary element: fog (unknown)
- Color: silver gray (neutral)

**Background story**:

"I used to work as a planner in a deterministic castle. I stepped into the foggy wasteland because I questioned the inherent rules. The compass I carried with me always pointed to a random direction..."

**Psychological mapping**:

- Career: Suitable for positions that require innovation, but be aware of the risk of goal dispersion
- Love: Enjoy the resonance of ideas, but fear the constraints of commitment
- Wealth: Wealth is just an exploration tool for him, not a goal

---

# Detailed report

## Introduction

## Detailed explanation of workflow map

The workflow describes the complete process of user interaction with the system, which can be understood through the following steps:

1. **User access and category selection**:
- The user accesses the tool through the web interface and first selects a category (such as career, love, wealth). This step determines the topic of the subsequent questions.
2. **System presents questions**:
- The system retrieves 10 questions related to the selected category from the database, each with 4 pictures corresponding to the predefined 20-30 roles.
- For example, if the user selects "love", the system may display questions such as "Choose the angel that attracts you most" and show 4 images generated from the character information.
3. **User answers questions**:
- The user selects an image for each question based on intuition or preference, and the system records the selection in real time.
- The user experience design needs to ensure that the interface is intuitive and the question design needs to be interesting (such as "Choose a picture based on your first impression").
4. **System collects selections**:
- The system collects all the user's choices for 10 questions and records them as data (such as choosing character A for question 1 and character B for question 2).
- Technically, the backend needs to process user input and the basic information behind the corresponding character.
5. **AI generates interpretation**:
- The system constructs prompt words based on user selections and categories, and sends them to the AI ​​model to generate interpretation text.
- For example, the prompt words may be: "The user selected Adventurer 3 times and Enthusiast 2 times in the Love category, and needs to refer to the basic information behind these characters to generate an interpretation of their love tendencies."
- The generated text returned by the AI ​​API needs to be relevant and unbiased.
6. **System displays results**:
- The system presents the interpretation text generated by AI to the user, which may be displayed in the form of a card or dialog box.

The simplified flowchart is represented as:

- **The user selects a category → The system presents 10 questions (4 pictures per question) → The user selects one by one → The system collects 10 choices → The system returns to check the basic information behind the role → Call AI API to generate interpretation → Display the results to the user.**

## Development Challenge

- AI-generated interpretations need to re-check the previous user's data (user selection, what role information the user's selected picture corresponds to), and we don't know if this part is difficult.
