# AGENTS.md

## Project overview

This project is a lunch recommendation agent. Its job is to help users find a random lunch spot based on location, cuisine, budget, distance, and dietary preferences.

## Product behavior

The agent should:
- Ask for location if one is not provided.
- Let the user enter city, ZIP code, or use browser geolocation.
- Search lunch-friendly restaurants near the user.
- Filter by open status, price, cuisine, distance, rating, and excluded categories.
- Randomly select one recommendation from the filtered list.
- Explain why the spot was chosen in 1–3 sentences.
- Provide 2 backup options.
- Avoid recommending closed places when open-hours data is available.
- Avoid repeating a previously selected restaurant during the same session.

## Development expectations

- Use TypeScript.
- Keep code readable and modular.
- Put API logic in `/lib`.
- Put UI components in `/components`.
- Store environment variable examples in `.env.example`.
- Never commit API keys.
- Add error handling for failed API calls.
- Add loading and empty-state UI.
- Run linting before opening a pull request.

## Testing expectations

Test these flows:
- User searches by ZIP code.
- User searches by city.
- User chooses cuisine.
- User excludes a cuisine.
- No restaurants are found.
- API key is missing.
- Restaurant API request fails.

## Security notes

- API keys must stay server-side.
- Do not expose secret keys in frontend code.
- Do not store precise user location unless the user explicitly enables saved preferences.
