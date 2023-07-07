
<h1 align="center" style="border:none !important">
    <code>laravel documentation for Console</code>
</h1>

<p align="center">
    <img src="https://raw.githubusercontent.com/millancore/lo/main/art/example.png" alt="Ladoc example" height="408">
    <p align="center">
        <a href="https://github.com/millancore/ladoc/actions"><img alt="GitHub Workflow Status (master)" src="https://img.shields.io/github/actions/workflow/status/millancore/ladoc/tests.yml"></a>
        <a href="https://packagist.org/packages/millancore/ladoc"><img alt="Total Downloads" src="https://img.shields.io/packagist/dt/millancore/ladoc"></a>
        <a href="https://packagist.org/packages/millancore/ladoc"><img alt="Latest Version" src="https://img.shields.io/packagist/v/millancore/ladoc"></a>
        <a href="https://packagist.org/packages/millancore/ladoc"><img alt="License" src="https://img.shields.io/packagist/l/millancore/ladoc"></a>
    </p>
</p>

------

**Ladoc** ladoc allows you to search and browse Laravel documentation in all its versions.

## Installation
**Requires [PHP 8.2](https://php.net/releases/)**

```bash
composer global require "millancore/ladoc"
```
## Usage

> **Tip:** To make it easier to use, create an alias, I usually use `zz`.

### Search

`ladoc <section> <query>`

```bash
ladoc blade @once
```
### List all sections

simply execute the command without parameters,  you will see a list of all the sections (in brackets).

```bash
ladoc
```
Result:
```
 Main List

• [0] Artisan Console (artisan)
• [1] Authentication (authentication)
• [2] Authorization (authorization)
• [3] Laravel Cashier (Stripe) (billing)
• [4] Blade Templates (blade)
... 
```
### Filter Main List
to simplify the navigation you can filter the list by initial letter 

```bash
ladoc -lv
```
Result:
```
 Main List | filter: V

• [85] Validation (validation)
• [87] Views (views)
```

### Navigation System
You can navigate through all sections using the indexes in the list. 

```bash
ladoc 4
```
Result:
```
 Blade Templates

• [0] Introduction (+)
• [1] Displaying Data (+)
• [2] Blade Directives (+)
...
```
and continue in that way

```bash
ladoc 4 2
```
Result:
```
Blade Directives

In addition to template inheritance and displaying data...

────────────────────────
• [0] If Statements
• [1] Switch Statements
• [2] Loops
• [3] The Loop Variable
...
```
### Using the search with index

You can search directly in a section using its index. `ladoc 4 @once` it's equal to `ladoc blade @once`.

### Versions

Ladoc allows you to search all versions of Laravel, just use `--brach` or `-b` to define the version you want to use.

```bash
ladoc -b5.2 blade
```
> If no version is set, use the latest one.

---

Ladoc is an open-sourced software licensed under the **[MIT license](https://opensource.org/licenses/MIT)**.



