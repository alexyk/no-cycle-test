# no-cycle-test

Test the `no-cycle` rule for eslint-plugin-import

There are three `.ts` files, `a.ts` and `b.ts` are circular imported each other, while `c.ts` imports both `a.ts` and `b.ts`.

ESLint should raise error when checking `c.ts` because the circular depencency exists.

But for some reason, running `yarn eslint src/c.ts` does **NOT** raise any error !!!
