# Firebase Pro

Provides rich language support, validation, navigation, and tooling for Firebase configuration and rules files.

Gain a comprehensive suite of Firebase development features directly in your favorite IDE:

- **Smart file recognition** for Firebase configuration, rules, and indexes files
- **Context-aware completion** for all Firebase-specific languages
- **Built-in schema validation** for correctness
- **Powerful inspections** and **quick fixes** for error prevention
- **Seamless navigation**, **documentation**, and **structure views**
- **Customizable formatting and color schemes** for a better development experience

This plugin streamlines Firebase configuration and rule authoring, reducing errors and improving productivity for teams
working with Firebase-backed projects.

---

# Firebase configuration file (`firebase.json`)

## File recognition

The plugin automatically recognizes the `firebase.json` file in the root directory of your project.  
Once detected, the file icon is replaced with a distinctive Firebase-specific icon, making it easily identifiable as the
Firebase configuration file.

## Completion

Enjoy intelligent code completion for your `firebase.json` configuration.  
The plugin provides context-aware suggestions for available keys and values — for example, typing `"data"` at the top
level suggests `"dataconnect"` and `"database"`.  
This helps configure Firebase faster and more accurately.

## Reference

Clickable references are provided for filenames linked within the Firebase configuration.  
When you reference files such as Firestore rules, Firestore indexes, Storage rules, or Realtime Database rules (e.g.,
`"firestore.rules"`), clicking the filename opens that file directly in the editor.

## Inspection

The plugin includes multiple inspections to help detect and fix configuration issues in `firebase.json`:

- Detects missing configurations for the default Firestore database.
- Detects duplicate configurations for the same Firestore database.
- Detects and offers quick fixes for missing Firestore Rules, Firestore Indexes, Storage Rules, and Realtime Database
  Rules files automatically creating them with default templates.

These and many other inspections help maintain a consistent and valid Firebase setup across your project.

## Schema Validation

The plugin validates that your `firebase.json` file adheres to Firebase’s official schema.  
It checks for invalid or missing properties to ensure the configuration is complete and deploy-ready.

---

# Firebase Security Rules

## File recognition

The plugin recognizes any `*.rules` files defined in the `firebase.json` file.  
It assigns unique icons for **Firestore Security Rules** and **Storage Security Rules**, helping you easily distinguish
rule types.

## Documentation

In-editor documentation is provided for all Firebase Security Rules language elements, including functions, variables,
interfaces, and their properties.  
For example, hovering over `request.auth.token` displays all authentication token properties with their descriptions.

## Completion

The plugin supports intelligent completion for:

- Built-in language constructs (functions, variables, interfaces, properties)
- Local variables and user-defined functions
- Path parameters
- Service-specific keywords for Firestore and Storage

## Inspection

Advanced inspections detect common issues such as:

- Recursive or overly deep function calls
- Invalid `allow` methods
- Invalid service names
- Incorrect type checks
- Undefined function calls

These and many other inspections help ensure your security rules are both syntactically valid and semantically correct,
reducing runtime errors and improving maintainability.

## Reference

Supports navigation from function calls to their declarations and variable usages, improving readability and
maintainability.

## Code style (formatting)

Provides a built-in formatter for Firebase Security Rules with customizable styling options in the IDE.

## Color scheme

Includes syntax highlighting for all Firebase Security Rules language elements with configurable colors and styles.

## Structure view

Displays a hierarchical **Structure View** showing services, match blocks, and functions, allowing easy exploration of
rule files.

---

# Firestore indexes

### File recognition

Recognizes Firestore index files configured in the `firebase.json` file and assigns a distinctive Firestore index icon
for easy identification.

### Completion

Provides auto-completion for Firestore index configuration keys and values.  
For example, typing `"co"` suggests `"collectionGroup"`.  
Suggestions follow the official Firestore index schema for defining composite and single-field indexes.

### Schema Validation

Validates Firestore index configuration files against the Firestore schema, ensuring:

- No invalid or unknown properties
- No missing required fields
- Correct data types

---

# Firebase Realtime Database Rules

## File recognition

Recognizes Firebase Realtime Database Rules files configured in `firebase.json`, assigning a unique icon that identifies
them as database rule files.

## Documentation

Provides in-editor documentation for all Firebase Realtime Database Rules language constructs.  
For example, hovering over `auth.token` shows its available properties and their descriptions.

## Completion

Offers intelligent completion for:

- Built-in functions, variables, interfaces, and properties
- Local variables such as `$location`

## Inspection

Includes inspections that detect:

- Use of `==` instead of strict `===`
- Undefined `$location` variable references

These and many other inspections provide real-time feedback, helping you maintain correct, clean, and consistent rule
definitions.

## Reference

Enables navigation for local variable references (e.g., `$location`) to quickly jump between definitions and usages.

## Code style (formatting)

Provides a built-in formatter for Firebase Realtime Database Rules with customizable styling options in the IDE.

## Color scheme

Adds a dedicated syntax highlighting scheme for Realtime Database Rules, with customizable color options for improved
readability.

## Structure view

Displays a hierarchical **Structure View** that presents a tree-like outline of the file’s contents.
