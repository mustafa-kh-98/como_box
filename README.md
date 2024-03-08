# como_box Package

This Flutter package provides a customizable dropdown without a list, allowing for a clean and straightforward selection experience.

## Usage

To use this package, add `como_box` to your `pubspec.yaml` file:

```yaml
dependency_overrides:
  como_box:
    git: https://github.com/mustafakh366/como_box
```

## Example Usage
```
CustomDropdown<T>(
  initialItem: initValue,
  isLoadingData: isLoadingData,
  emptyText: "No items available",
  noResultFoundText: items.isEmpty ? "No items found" : null,
  hintBuilder: (_, __) {
    return TextWidget(
      hint,
      textAlign: TextAlign.start,
      textStyle: context.fontTitle12NormalGray,
    );
  },
  excludeSelected: true,
  expandedBorderRadius:expandedBorderRadius,
  items: items,
  closedFillColor: Colors.white,
  closedBorder: closedBorder,
  closedSuffixIcon:closedSuffixIcon,
  expandedSuffixIcon: expandedSuffixIcon,
  listItemBuilder: expandedListItemBuilder,
  headerBuilder: selectedItemBuilder,
  hideSelectedFieldWhenExpanded: true,
  searchHintText: "Search items...",
  splashColor:splashColor ,
  hoverColor: hoverColor,
  closedBorderRadius: closedBorderRadius,
  onChanged: onChanged,
  validator: (value) {
    if (value == null || value.toString().isEmpty) {
      return "This field is required";
    }
    return null;
  },
  closedErrorBorder:closedErrorBorder,
  closedErrorBorderRadius:closedErrorBorderRadius,
  errorStyle:errorStyle,
)
```
## Example Usage With Search
```
CustomDropdown<T>.search(
            emptyText:"No items available",
            isLoadingData: isLoadingData,
            noResultFoundText: items.isEmpty ? "No items found" : null,
            hintBuilder: (_, __) {
              return TextWidget(
                hint,
                textAlign: TextAlign.start,
                textStyle: context.fontTitle12NormalGray,
              );
            },
            initialItem: initValue,
            excludeSelected: true,
            expandedBorderRadius: BorderRadius.circular(5),
            items: items,
            closedFillColor: Colors.white,
            closedBorder:closedBorder ,
            closedSuffixIcon:closedSuffixIcon,
            expandedSuffixIcon:expandedSuffixIcon,
            listItemBuilder: expandedListItemBuilder,
            headerBuilder: selectedItemBuilder,
            hideSelectedFieldWhenExpanded: true,
            searchHintText: searchHint,
            splashColor:splashColor,
            hoverColor: hoverColor,
            closedBorderRadius: closedBorderRadius,
            onChanged: onChanged,
            validator: (value) {
              if (value == null || value.toString().isEmpty) {
                return ";
              }
              return null;
            },
            closedErrorBorder: closedErrorBorder,
            closedErrorBorderRadius: closedErrorBorderRadius,
            errorStyle: errorStyle,
          ) 
    ```
    
