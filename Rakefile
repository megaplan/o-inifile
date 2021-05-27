
begin
  require 'bones'
rescue LoadError
  abort '### please install the "bones" gem ###'
end

ensure_in_path 'lib'
require 'inifile'

task :default => 'test:run'
task 'gem:release' => 'test:run'

Bones {
  name         'o-inifile'
  summary      'INI file reader and writer'
  authors      'Oleg Pudeyev'
  email        'code@olegp.name'
  url          'https://github.com/p/o-inifile'
  version      IniFile::VERSION

  use_gmail
  depend_on    'bones-git', "~> 1.3", :development => true
}
