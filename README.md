## Flask Application Design for Coiffeur Jass Score Counting:

**HTML Files:**

- `index.html`: The main page of the application that allows users to input their scores.
- `results.html`: A page that displays the final score and provides an option to start a new game.

**Routes:**

- **`/`**: The route corresponding to the index page, where users can enter scores.
- **`/calculate-score`**: A POST route that receives the submitted scores for calculation.
- **`/new-game`**: A GET route that generates a new index page, allowing users to start a new game.

**Explanation:**

**1. HTML Files:**

- `index.html`:
   - Contains a form for users to enter their scores and submit the request.
   - The form sends a POST request to `/calculate-score` when submitted.
- `results.html`:
   - Shows the calculated score, providing information about the winning team and the individual scores.
   - Includes a button that redirects users to a new index page via the `/new-game` route.

**2. Routes:**

- **`/`** (index page):
   - Renders the `index.html` page when accessed.
- **`/calculate-score`**:
   - Receives the submitted scores through a POST request.
   - Calculates the score according to the Coiffeur Jass rules.
   - Renders the `results.html` page, passing the calculated score.
- **`/new-game`**:
   - Generates a new index page by rendering `index.html`.
   - Allows users to start a new game by reloading the score input interface.