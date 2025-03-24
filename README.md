# WordPress Cursor AI Rules

This repository contains a collection of Cursor AI rules specifically designed for WordPress development, helping developers build better WordPress plugins, themes, and products with AI assistance.

## What are Cursor Rules?

[Cursor](https://cursor.com/) is an AI-first code editor built on VSCode. Cursor Rules allow you to customize the AI's behavior by providing specific instructions and guidelines. These rules help the AI understand your project's context, coding standards, and best practices, resulting in more accurate and helpful AI assistance.

Learn more about [Cursor Rules](https://docs.cursor.com/context/rules-for-ai) in the official documentation.

## Features

- **Plugin Development Rules**: Guidelines for WordPress plugin development including PHP standards, JavaScript best practices, and WordPress core integration.
- **Theme Development Rules**: Comprehensive rules for theme development, with special focus on block themes (Full Site Editing).
- **WordPress Coding Standards**: Rules aligned with WordPress coding standards and best practices.
- **Modern Development**: Support for modern WordPress development techniques including React, webpack, and block-based features.

## How to Use These Rules

1. **Clone or copy the example rules**: Choose either the plugin or theme example based on your project type.
2. **Create a `.cursor` directory**: In your WordPress project's root, create a `.cursor` directory if it doesn't exist.
3. **Add the rules**: Copy the relevant rules from the examples into your `.cursor/rules` directory.
4. **Customize the rules**: 
   - Replace any `myprefix_` with your plugin or theme prefix
   - Modify the rules to match your specific project requirements
   - Add or remove rules based on your project's needs (e.g., remove webpack rules if not applicable)
5. **Restart Cursor**: After adding or modifying rules, restart Cursor to apply the changes.

## How Cursor Rules Are Loaded

Cursor Rules are automatically loaded when you're working in a project that contains a `.cursor/rules` directory. The rules apply in the following ways:

- **Automatic Loading**: Rules with `alwaysApply: true` are always loaded when working in the project.
- **File Pattern Matching**: Rules with specific `globs` patterns (e.g., `*.php`, `*.js`) are loaded when working with matching files.
- **Manual Addition to Context**: Rules without `alwaysApply` and not matching file patterns can be manually added to the context by selecting them in the Cursor sidebar under "Rules".

Cursor prioritizes rules based on specificity - file-specific rules take precedence over general rules. When multiple rules apply, their instructions are combined to guide the AI.

To refresh rules after editing them, you can either restart Cursor or use the "Reload Rules" option in the Cursor menu.

With this information in mind, please review each file and adjust the rule loading as you need it. For example, the git.mdc file should not be loaded with alwaysApply, because that rule should be called manually only when you are preparing a commit.

## Contributing

Contributions are welcome! If you have improvements to existing rules or new WordPress-specific rules that would be helpful for the community, please submit a pull request.

## License

This project is licensed under [GPL3 License](LICENSE).