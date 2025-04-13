# Vibe Components CLI

CLI tool to add Vibe Components and Cursor rules to your React project.

## Installation & Usage

There are two ways to use this tool:

### Option 1: Install globally

```bash
# Install globally
npm install -g vibe-components-cli

# Then use from any project
vibe-components add
```

### Option 2: Use with npx (no installation)

```bash
# Run directly with npx
npx vibe-components-cli add
```

## What it does

Running the `add` command will:

1. Install the following npm packages:
   - [vaul](https://vaul.emilkowal.ski/) - A drawer component for React
   - [@number-flow/react](https://number-flow.barvian.me/) - An animated number component for React
   - [sonner](https://sonner.emilkowal.ski/) - An opinionated toast component for React

2. Create a `.cursor/rules.json` file with component snippets for the Cursor IDE

## Components

### Vaul Drawer

A performant and accessible bottom sheet component.

```jsx
import { Drawer } from 'vaul';

function MyComponent() {
  return (
    <Drawer.Root>
      <Drawer.Trigger>
        <button>Open Drawer</button>
      </Drawer.Trigger>
      <Drawer.Portal>
        <Drawer.Overlay className="fixed inset-0 bg-black/40" />
        <Drawer.Content className="bg-white flex flex-col rounded-t-[10px] h-full mt-24 max-h-[85vh] fixed bottom-0 left-0 right-0">
          <div className="p-4 rounded-t-[10px] flex-1">
            <div className="mx-auto w-12 h-1.5 bg-gray-300 rounded-full mb-4" />
            <div className="max-w-md mx-auto">
              <h2>Drawer Content</h2>
            </div>
          </div>
        </Drawer.Content>
      </Drawer.Portal>
    </Drawer.Root>
  );
}
```

### NumberFlow

An animated number component.

```jsx
import NumberFlow from '@number-flow/react';

function MyComponent() {
  const [value, setValue] = useState(123);

  return <NumberFlow value={value} />;
}
```

### Sonner Toast

An opinionated toast component.

```jsx
import { Toaster, toast } from 'sonner';

function MyComponent() {
  return (
    <>
      <Toaster />
      <button onClick={() => toast('My first toast')}>Show toast</button>
    </>
  );
}
```

## License

ISC 