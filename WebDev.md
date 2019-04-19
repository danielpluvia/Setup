# NodeJS

## Solution

### Absolute Paths for Create-React-Native-App Expo TypeScript

For compiler, so that it can run without a error:

Create a `.env` file under the root path. Add `NODE_PATH=./` to it.

---

For VSCode:

Note: The following codes are for VSCode, so that users can command+click to jump to the code.

Create a `jsconfig.json` file and add the following code to it:

```json
{
  "compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "src/*": ["./src/*"]
    }
  }
}
```

In the `./src` folder, I added a `package.json` file with the below content:

```json
{
  "name": "src"
}
```

### Usage

```js
import LoginPage from 'src/pages/Login';
```

## References

[Absolute Paths for Create-React-Native-App Expo TypeScript](https://medium.com/val-punk/absolute-paths-for-create-react-native-app-expo-typescript-d32942b4b230)