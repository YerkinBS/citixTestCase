# Instagram Real Estate Post Generator

This project uses OpenAI's GPT-3.5-turbo API to generate captivating and sales-oriented Instagram posts for real estate listings. The posts are based on random entries from the Housing Prices Dataset, providing varied and engaging real estate content.

## Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/YerkinBS/citixTestCase.git
    cd citixTestCase
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Create a `.env` file in the project root and add your OpenAI API key:

    ```bash
    openai_token=your_openai_api_key
    ```

4. Open and run the `main.ipynb` Jupyter Notebook:

    ```bash
    jupyter notebook main.ipynb
    ```

## Project Structure

- **main.ipynb**: The main script to generate Instagram posts using OpenAI GPT-3.5-turbo API.
- **Housing.csv**: The dataset containing housing prices entries.
- **EXAMPLE.md**: Examples of generated Instagram posts.
- **.env**: Configuration file for storing OpenAI API key.
- **requirements.txt**: List of project dependencies.

## Example Generated Posts

See [EXAMPLE.md](EXAMPLE.md) for examples of generated Instagram posts.

## Questions

### How to mimic the style of successful Instagram posts?
The history of conversations with the model informs the style. To determine the model's tone and style, we can play around with various prompt engineering strategies and make adjustments to the input messages.

### What prompt engineering techniques can improve quality?

- Test out different message roles (assistant, system, and user).
- In user messages, give succinct and understandable information.
- Adapt the prompt to help the model produce the desired results. 

### How to ensure the model doesn't invent extra features?

When sending user messages, be explicit and detailed so that the model can concentrate on the important aspects. For best outcomes, review and modify prompts on a regular basis.

## Additional Information

The reason why I chose to write the script in the **.ipynb** file rather than **.py** file is the more structured code and ability to run only needed parts of code. It helps to avoid the loading of dataset and initializing GPT client each time we're generating the post. Just run all cells once and then if we want more post generating we can run just one cell where generating logic script is writed. We can do this every time until token limit is not exceeded. Else we just re-initialize our GPT Client by re-running all cells of code.
And the reason why I didn't use the DALLE3 API is because I used 0.27.0 version of OpenAI ChatGPT gpt3.5-turbo API.
I hope everything is clear and I'll be waiting for feedback!