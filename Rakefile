file ".git/hooks/post-commit" do |t|
  File.open(t.name, "w") { |f| f.puts "rake PortIndex" }
  sh "chmod +x #{t.name}"
end

desc "Rebuild the Port index."
file "PortIndex" => Dir["**/Portfile"] do
  sh "portindex"
end

desc "Install post-commit hook, rebuild Port index."
task :setup => %w(.git/hooks/post-commit PortIndex)

task :default => :setup
