# Textarea Field

```php
SixaSnippets\Dashboard\Options::textarea_field( array $args = array(), bool $echo = true );
```

## Description

Output a textarea input box.

## Import

```php 
use SixaSnippets\Dashboard\Options;
```

## Parameters

- **$args**
    - **id**:
        - *(string) (Required)* Slug-name to identify the field. Used in the 'id' attribute of tags.
    - **name**:
        - *(string) (Optional)* Can be used to reference the element in other places.
        - *Default value: $id*
    - **label**:
        - *(string) (Optional)* Formatted title of the field.
    - **description**:
        - *(string) (Optional)* A help text will be shown below the input field.
    - **placeholder**:
        - *(string) (Optional)* A string that provides a brief hint to the user.
    - **class**:
        - *(string) (Optional)* Custom CSS class names to be added to the input field.
        - *Default value: short*
    - **wrapper_class**:
        - *(string) (Optional)* Custom CSS class names to be added to the input field wrapper paragraph tag.
    - **style**:
        - *(string) (Optional)* Inline style may be used to apply a unique style to the input field.
    - **value**:
        - *(string) (Optional)* The current value of the input field.
    - **rows**:
        - *(integer) (Optional)* The visible number of lines.
        - *Default value: 2*
    - **cols**:
        - *(integer) (Optional)* The visible width of the textarea.
        - *Default value: 20*
    - **custom_attributes**:
        - *(array) (Optional)* Attributes consist of two parts:
            - The attribute name should not contain any uppercase letters, and must be at least one character long after the prefix.
            - The attribute value can be any thing.
- **$echo**
    - *(bool) (Optional)* Whether to echo or just return the output.
    - *Default value: true*

## Example

```php
Options::textarea_field(
	array(
		'label'             => __( 'Textarea field', '@@textdomain' ),
		'description'       => __( 'More information about this field.', '@@textdomain' ),
		'placeholder'       => __( 'Write content…', '@textdomain' ),
		'class'             => 'short',
		'style'             => 'color:#A8A8A8;',
		'wrapper_class'     => 'wrapper-class-name',
		'value'             => 'textarea value',
		'id'                => 'sixa_options_textarea',
        'rows'              => 2,
        'cols'              => 20,
		'custom_attributes' => array(
			'data-attr' => 'attr-value',
		),
	)
);
```