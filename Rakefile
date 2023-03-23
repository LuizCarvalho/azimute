#
# To change this template, choose Tools | Templates
# and open the template in the editor.

require 'rubygems'
require 'rake'
require 'rake/clean'
require 'rake/gempackagetask'
require 'rake/rdoctask'
require 'rake/testtask'

spec = Gem::Specification.new do |s|
  s.name = 'azimute'
  s.version = '0.0.1'
  s.has_rdoc = true
  s.extra_rdoc_files = %w[README LICENSE]
  s.summary = 'Gerador de polígonos para representação de Contornos de Propagação para Radiodifusão com plotagem em sistema GIS do Google Earth, a partir de ângulo ( Azimute) e distância fornecidos'
  s.description = s.summary
  s.author = 'Luiz Carvalho'
  s.email = 'maximusmano@gmail.com'
  # s.executables = ['your_executable_here']
  s.files = %w[LICENSE README Rakefile] + Dir.glob('{bin,lib,spec}/**/*')
  s.require_path = 'lib'
  s.bindir = 'bin'
end

Rake::GemPackageTask.new(spec) do |p|
  p.gem_spec = spec
  p.need_tar = true
  p.need_zip = true
end

Rake::RDocTask.new do |rdoc|
  files = ['README', 'LICENSE', 'lib/**/*.rb']
  rdoc.rdoc_files.add(files)
  rdoc.main = 'README' # page to start on
  rdoc.title = 'Azimute Docs'
  rdoc.rdoc_dir = 'doc/rdoc' # rdoc output folder
  rdoc.options << '--line-numbers'
end

Rake::TestTask.new do |t|
  t.test_files = FileList['test/**/*.rb']
end
