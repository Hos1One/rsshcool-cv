# Danila Kahanchik

## My Contact Info
- **Address:** Belarus, Gomel
- **Phone:** +375 (29) 648-92-98
- **E-mail:** [kahanchikd@gmail.com](kahanchikd@gmail.com)
- **GitHub:** [Hos1One](https://github.com/Hos1One)

## Summary
Fast run course

## Skills
- **HTML**
- **CSS** 
  - Framework: Bootstrap
  - Preprocessor: SCSS
  - Methodology: BEM
- **Version control:** Git (remote service GitHub)
- **C** (basic knowledge), **Python** (basic knowledge) 
  - Framework: Flask (basic knowledge)
  - Database: SQLite (basic knowledge)
- **Operating Systems:** Windows, Linux (Ubuntu/Kubuntu)


## Code Examples
```Linux
#!/bin/bash

CONFIG_FILE="/etc/network/interfaces"

function display_config {
    echo "Текущие настройки сетевых интерфейсов:"
    cat $CONFIG_FILE
}

function update_interface {
    local interface=$1
    shift
    local new_config="$@"

    if grep -q "^auto $interface" $CONFIG_FILE; then
        sed -i "/^auto $interface/,/^$/c\\auto $interface\n$new_config" $CONFIG_FILE
    else
        echo -e "\nauto $interface\n$new_config" >> $CONFIG_FILE
    fi

    echo "Настройки интерфейса $interface обновлены."
}

if [[ $1 == "display" ]]; then
    display_config
elif [[ $1 == "update" ]]; then
    if [[ $# -lt 3 ]]; then
        echo "Использование: $0 update <интерфейс> <новые настройки>"
        exit 1
    fi
    update_interface "$2" "${@:3}"
else
    echo "Использование: $0 {display|update}"
fi
}

const longestWord = findLongestWord("Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent rutrum, quam sit amet semper tempus, velit nibh pellentesque dui, nec consectetur erat orci et libero.");
console.log(longestWord);
