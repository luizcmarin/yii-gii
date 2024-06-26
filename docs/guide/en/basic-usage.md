Basic Usage
===========

When you open Gii you first see the entry page that lets you choose a generator.

![Gii entry page](../../images/gii-entry.png)

By default there are the following generators available:

- **Model Generator** - This generator generates an ActiveRecord class for the specified database table.
- **CRUD Generator** - This generator generates a controller and views that implement CRUD (Create, Read, Update, Delete)
  operations for the specified data model.
- **Controller Generator** - This generator helps you to quickly generate a new controller class, one or several
  controller actions and their corresponding views.
- **Form Generator** - This generator generates a view script file that displays a form to collect input for the
  specified model class.
- **Module Generator** - This generator helps you to generate the skeleton code needed by a Yii module.
- **Extension Generator** - This generator helps you to generate the files needed by a Yii extension.

After choosing a generator by clicking on the "Start" button you will see a form that allows you to configure the
parameters of the generator. Fill out the form according to your needs and press the "Preview" button to get a
preview of the code that Gii is about to generate. Depending on the generator you chose and whether the files
already existed or not, you will get an output similar to what you see in the following picture:

![Gii preview](../../images/gii-preview.png)

Clicking on the file name you can view a preview of the code that will be generated for that file.
When the file already exists, Gii also provides a diff view that shows what is different between the code that exists
and the one that will be generated. In this case you can also choose which files should be overridden and which not.

> Tip: When using the Model Generator to update models after database change, you can copy the code from Gii preview
  and merge the changes with your own code. You can use IDE features like PHPStorms
  [compare with clipboard](https://www.jetbrains.com/help/phpstorm/comparing-files-and-folders.html), [Aptana Studio](https://www.aptana.com/products/studio3/download) or [Eclipse](https://www.eclipse.org/pdt/) based editor also allows [compare with clipboard](https://andrei.gmxhome.de/anyedit/examples.html) by using [AnyEdit tools plugin](https://andrei.gmxhome.de/anyedit/) for this, which allows you to merge in relevant changes and leave out others that may revert your own code.
  
After you have reviewed the code and selected the files to be generated you can click the "Generate" button to create
the files. If all went fine you are done. When you see errors that Gii is not able to generate the files you have to
adjust directory permissions so that your webserver is able to write to the directories and create the files.

> Note: The code generated by Gii is only a template that has to be adjusted to your needs. It is there
  to help you create new things quickly but it is not something that creates ready to use code.
  We often see people using the models generated by Gii without change and just extend them to adjust
  some parts of it. This is not how it is meant to be used. Code generated by Gii may be incomplete or incorrect
  and has to be changed to fit your needs before you can use it.
  