##### Atom and all repositories under Atom will be archived on December 15, 2022. Learn more in our [official announcement](https://github.blog/2022-06-08-sunsetting-atom/)
 # space-pen-example Templates

This provides a set of templates for `apm init` to generate a new Atom package using space-pen as the view system.

![screen shot 2014-12-03 at 2 45 25 pm](https://cloud.githubusercontent.com/assets/69169/5290378/150beeee-7afb-11e4-8d76-6a42575fe03f.png)

These templates are an alternative to a package generated in atom via the `package-generator:generate-package` command, substituting space-pen in for manual DOM manipulation.

## Usage

You supply the templates in the `templates` dir to `apm init`

```
git clone git@github.com:atom/space-pen-example-templates.git
apm init -p my-package-name --template space-pen-example-templates/templates
```

Now you should have a new package in the `my-package-name` directory. Now you can link it and see it in action

```
cd my-package-name
apm install
apm link -d
atom -d
```

In Atom use the `ctrl-alt-o` key command to see it in action.

## More info

The resulting package has only one dependency: [`atom-space-pen-views`](https://github.com/atom/atom-space-pen-views). Through `atom-space-pen-views`, all of [`space-pen`](https://github.com/atom/space-pen) is available as well as Atom-specific views like `TextEditorView` for mini editors, and `SelectListView` for a selectable list of items.
