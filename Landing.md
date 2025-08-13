# Guide to Editing the BSV Hub Landing Page in Markdown Mode

This guide assumes you have Creator/Admin permissions in your GitBook organization and are working on the unified docs site (BSV Hub). It focuses on editing the landing page's "code" in Markdown for trial changes, without affecting the live site until you publish.

## Step 1: Access the Landing Page Editor
- Log in to GitBook and navigate to your organization dashboard.
- In the sidebar, select the unified docs site (e.g., "BSV Hub").
- Open the content editor from the site's dashboard.
- Locate the landing page in the content tree (left sidebar)—it's usually the homepage (confirm in **Settings** > **Navigation**).
- Click to open the page.

## Step 2: Switch to Markdown Mode
- In the editor interface, look for the Markdown toggle in the top-right corner (it may be labeled "Markdown," "Code," or shown as a `< >` icon).
- Click it to switch from visual mode to raw Markdown view.
- You'll see the page's content as plain Markdown text, including GitBook-specific blocks like:
  - Headings: `# Welcome to BSV Hub`
  - Cards: `{% card title="BSV Case Study Library" ... %}`
  - Buttons: `{% button text="Technical Info" ... %}`
  - Columns: `{% columns %} ... {% endcolumns %}`

## Step 3: Make Trial Edits in Markdown
- Edit the text directly:
  - Change a heading: Modify lines like `# Welcome to BSV Hub` to `# Test Welcome Page`.
  - Update a card (big button): Find a block like `{% card title="BSV Case Study Library" description="Real-world applications." url="/case-studies" buttonText="Go to Case Studies" buttonStyle="primary large" %}` and tweak the `title`, `description`, `url`, or `buttonText` (e.g., change `url` to `/test-path` for testing).
  - Adjust a filter button: Edit `{% button text="Technical Info" url="/filters/technical" style="secondary large" icon="code" %}` to something like `{% button text="Test Filter" url="/test" style="secondary large" icon="star" %}`.
  - Add a new button: Copy an existing block and paste it below, then customize (e.g., duplicate a `{% button %}` and change its details).
  - Remove elements: Delete entire blocks (e.g., remove a `{% card %}` section by erasing its lines).
- Use GitBook's extended Markdown syntax for blocks (e.g., `{% hint style="info" %}Your note here{% endhint %}` for tips).
- Experiment freely—auto-saves keep your changes as drafts.

## Step 4: Preview and Test Changes
- Switch back to visual mode using the same toggle to see how edits render (e.g., big buttons in a grid).
- Use the preview button (eye icon, top-right) to test the page without publishing:
  - Click buttons/cards to check links (they should navigate to sections like `/case-studies`).
  - Verify layout on desktop/mobile.
- If something breaks, undo via the editor's history (top menu > Version history) or revert to the original.

## Step 5: Save Without Publishing
- Changes stay in draft mode—don't click "Publish" for non-serious trials.
- If you want to test live temporarily, publish a draft version, then roll back via history.
- For safety, duplicate the page first (right-click in content tree > Duplicate) and edit the copy.

## Tips and Troubleshooting
- **Common Issues**: If blocks don't render, check syntax (e.g., close tags like `{% endcard %}`). GitBook docs have examples.
- **No Repo Needed**: All edits happen in GitBook—no GitHub involvement required.
- **Limitations**: For advanced styling, add custom CSS in **Settings** > **Customization** > **Custom code**, but stick to Markdown for simple trials.
- If the toggle isn't visible or you get errors, try refreshing or contact GitBook support with your org details.

This keeps everything safe and reversible. Once you're happy with trials, you can apply them to the live site.
