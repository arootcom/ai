# Gvim-AI

## Установка vim-plugin

```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

## Установка плагина vim-ollama (через vim-plug)

Репозиторий кода плагина [Ollama Support for Vim](https://github.com/gergap/vim-ollama)

Добавить в <code>~/.gvimrc</code>

```
" Начало блока плагинов
call plug#begin()

" Плагин для интеграции с Ollama
Plug 'gergap/vim-ollama'

" Конец блока плагинов
call plug#end()
```

После этого выполнить в Gvim <code>:PlugInstall</code>
Если всё прошло успешно, будет статус <code>Finishing ... Done!</code>.

## Зависимости

```
sudo apt install python3-httpx python3-jinja2 python3-requests
```

## Базовые настройки для связи с моделью

Добавить в <code>~/.gvimrc</code>

```
" Принудительно подключаем плагин
set runtimepath+=~/.vim/plugged/vim-ollama
" Явно загружаем исполняемый файл плагина
source ~/.vim/plugged/vim-ollama/plugin/ollama.vim
```

После внесения изменений в .vimrc перезапустить Gvim или выполнить команду <code>:source ~/.vimrc</code>.

Запускаем процедуру автоматической конфигурации <code>:Ollama setup<code>


## Умное дополнение кода (как GitHub Copilot)



