| Lookup           | Description                                            | Usage                                                 | Example                                                |
|------------------|--------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| `contains`       | Case-sensitive containment test                        | `queryset.filter(field_name__contains=value)`            | `queryset.filter(content__contains='search term')`       |
| `icontains`      | Case-insensitive containment test                      | `queryset.filter(field_name__icontains=value)`          | `queryset.filter(title__icontains='term')`               |
| `regex`          | Matches a field value using a regular expression       | `queryset.filter(field_name__regex=r'regular expression')` | `queryset.filter(content__regex=r'^\d{4}$')`             |
| `iregex`         | Case-insensitive regex match                           | `queryset.filter(field_name__iregex=r'regular expression')`| `queryset.filter(title__iregex=r'^search')`              |
| `search`         | Full-text search using the database's search capability| `queryset.filter(field_name__search='search term')`     | `queryset.filter(content__search='query')`                |
| `startswith`     | Case-sensitive starts-with test                        | `queryset.filter(field_name__startswith=value)`         | `queryset.filter(name__startswith='start')`               |
| `istartswith`    | Case-insensitive starts-with test                      | `queryset.filter(field_name__istartswith=value)`       | `queryset.filter(title__istartswith='start')`             |
| `endswith`       | Case-sensitive ends-with test                          | `queryset.filter(field_name__endswith=value)`           | `queryset.filter(name__endswith='end')`                   |
| `iendswith`      | Case-insensitive ends-with test                        | `queryset.filter(field_name__iendswith=value)`         | `queryset.filter(title__iendswith='end')`                 |
| `isnull`         | Checks if the field value is null                      | `queryset.filter(field_name__isnull=True)`              | `queryset.filter(date__isnull=True)`                      |
| `exists`         | Checks if there is at least one related object         | `queryset.filter(field_name__exists=True)`              | `queryset.filter(tags__exists=True)`                      |
| `gt`             | Greater than                                          | `queryset.filter(field_name__gt=value)`                 | `queryset.filter(price__gt=100)`                          |
| `gte`            | Greater than or equal to                              | `queryset.filter(field_name__gte=value)`                | `queryset.filter(quantity__gte=10)`                       |
| `lt`             | Less than                                             | `queryset.filter(field_name__lt=value)`                 | `queryset.filter(price__lt=100)`                          |
| `lte`            | Less than or equal to                                 | `queryset.filter(field_name__lte=value)`                | `queryset.filter(quantity__lte=50)`                       |
| `range`          | Range test                                            | `queryset.filter(field_name__range=(start_value, end_value))` | `queryset.filter(age__range=(18, 65))`                   |
| `year`           | Matches the year value of the field                   | `queryset.filter(field_name__year=value)`               | `queryset.filter(birth_date__year=1990)`                  |
| `month`          | Matches the month value of the field                  | `queryset.filter(field_name__month=value)`              | `queryset.filter(birth_date__month=12)`                   |
| `day`            | Matches the day value of the field                    | `queryset.filter(field_name__day=value)`                | `queryset.filter(birth_date__day=25)`                     |
| `hour`           | Matches the hour value of the field                   | `queryset.filter(field_name__hour=value)`               | `queryset.filter(created_at__hour=14)`                    |
| `minute`         | Matches the minute value of the field                 | `queryset.filter(field_name__minute=value)`             | `queryset.filter(created_at__minute=30)`                  |
| `second`         | Matches the second value of the field                 | `queryset.filter(field_name__second=value)`             | `queryset.filter(created_at__second=0)`                   |
| `week_day`       | Matches the day of the week (0-6, where 0=Sunday)     | `queryset.filter(field_name__week_day=value)`           | `queryset.filter(created_at__week_day=1)`                 |
| `iso_year`       | Matches the ISO year of the field                     | `queryset.filter(field_name__iso_year=value)`           | `queryset.filter(created_at__iso_year=2023)`              |
| `iso_week`       | Matches the ISO week of the year                      | `queryset.filter(field_name__iso_week=value)`           | `queryset.filter(created_at__iso_week=12)`                |
| `iso_week_day`   | Matches the ISO day of the week (1-7, where 1=Monday) | `queryset.filter(field_name__iso_week_day=value)`       | `queryset.filter(created_at__iso_week_day=5)`             |
| `contains_text`  | Full-text search (works on PostgreSQL only)           | `queryset.filter(field_name__contains_text='search term')` | `queryset.filter(content__contains_text='query')`        |
| `contained_by`   | Checks if value is contained by field (works on arrays) | `queryset.filter(field_name__contained_by=[value1, value2])` | `queryset.filter(tags__contained_by=['tech', 'news'])`   |
| `overlap`        | Checks if values overlap field (works on arrays)      | `queryset.filter(field_name__overlap=[value1, value2])`  | `queryset.filter(tags__overlap=['django', 'python'])`    |
| `len`            | Matches length of field (works on arrays)             | `queryset.filter(field_name__len=value)`                | `queryset.filter(tags__len=2)`                           |
