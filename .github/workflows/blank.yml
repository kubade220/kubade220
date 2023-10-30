name: Update Latest Medium Blogs

on:
  schedule:
    - cron: "0 0 * * *"  # Runs the job daily

jobs:
  update-blogs:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Python
        uses: actions/setup-python@v2
        with:
          python-version: 3.x  # Choose the appropriate Python version

      - name: Install dependencies
        run: pip install requests

      - name: Update Latest Medium Blogs
        run: python update_blogs.py  # Replace with your script

      - name: Commit and push changes
        run: |
          git config user.name "kubade220"
          git config user.email "kubix114@wp.pl"
          git add .
          git commit -m "Update latest Medium blogs"
          git push
