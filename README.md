# lockwright-utils-password-generator

An utility package for generating secure passwords and passphrases.

Site: [lockwright.dexterity.works](https://lockwright.dexterity.works)

Community fork of PearPass (Apache 2.0). Not affiliated with or endorsed by Tether Data or the Pears project.

## Table of Contents
- [Features](#features)
- [Security Notice](#security-notice)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Dependencies](#dependencies)
- [Related Projects](#related-projects)

## Features

- Generate secure passwords with customizable options
    - Configurable length
    - Include/exclude special characters
    - Include/exclude lowercase letters
    - Include/exclude uppercase letters
    - Include/exclude numbers
- Generate memorable passphrases with configurable settings
    - Adjustable word count
    - Optional capitalization
    - Optional number suffixes
    - Optional symbol suffixes

## Security Notice

Imports stay `@tetherto/pearpass-utils-password-generator`. That npm name is not this fork if you install it from the npm registry.

## Installation

```bash
npm install git+https://github.com/Dexterity-Works/lockwright-utils-password-generator.git
```

## Usage Examples
```javascript
import { generatePassword, generatePassphrase } from '@tetherto/pearpass-utils-password-generator';

// Generate a password
const password = generatePassword(12, {
    includeSpecialChars: true,
    lowerCase: true,
    upperCase: true,
    numbers: true
});

// Generate a passphrase
const passphrase = generatePassphrase(true, true, true, 4);
```

### Password Generation
```javascript
// Generate a 16-character password with all character types
const strongPassword = generatePassword(16);

// Generate a 12-character password without special characters
const simplePassword = generatePassword(12, { includeSpecialChars: false });

// Generate a numeric PIN
const pin = generatePassword(6, {
    includeSpecialChars: false,
    lowerCase: false,
    upperCase: false,
    numbers: true
});
```

### Passphrase Generation
```javascript
// Generate a 4-word passphrase with capitalization, symbols, and numbers
const complexPassphrase = generatePassphrase(true, true, true, 4);
// Example: "Guitar5$ Elephant3# Balloon7^ Dog2&"

// Generate a simple 3-word passphrase
const simplePassphrase = generatePassphrase(false, false, false, 3);
// Example: "river camera piano"
```

## Dependencies

This package has no production dependencies.

## Related Projects

- [lockwright-app-mobile](https://github.com/Dexterity-Works/lockwright-app-mobile) - Lockwright for mobile
- [lockwright-app-desktop](https://github.com/Dexterity-Works/lockwright-app-desktop) - Lockwright for desktop
- [lockwright-lib-ui-react-native-components](https://github.com/Dexterity-Works/lockwright-lib-ui-react-native-components) - Lockwright UI kit
- [tether-dev-docs](https://github.com/Dexterity-Works/tether-dev-docs) - Documentations and guides for developers

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](./LICENSE) file for details.