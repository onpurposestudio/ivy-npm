# Ivy CLI by OnPurpose Studio

The Ivy CLI tool helps dev teams and LLM's observe and manage translation files in their local codebase.

- Use `ivy resource` commands to work with your Resource Files
- Use `ivy key` commands to manage individual keys across Resource Files
- use `ivy translate` commands to translate content using your preferred local agent

## Install

```
npm i -g @onpurposestudio/ivy
```

## Documentation

We've baked our entire documentation into `ivy --help` itself. This makes it very easy for LLM's to move as quickly as you do.

```
$ ivy --help
Ivy for Dev Teams
This is a CLI tool that dev teams and LLMs can use to simplify the process
of managing and translating content within their codebase.

Ivy is paid software available to clients of OnPurpose Studio. If you'd
like a license, please reach out:

✉️ hello@onpurpose.studio
🌎 https://onpurpose.studio

Usage: ivy [command] [options]

Commands:
 auth                These commands help manage your auth token and   
                     other logistics relevant to your account with    
                     OnPurpose Studio                                 
                                                                      
 key                 These commands provide insight to translation    
                     keys across all the locales in your codebase.    
                                                                      
 resource            These commands provide insight to Resource       
                     Files, which often contain translations for one  
                     locale across many keys (but not always)         
                                                                      
 translate           These commands help with the process of          
                     translating content within this codebase.        
                                                                      

Options:
 --root              Root directory for the codebase. In the case of  
                     a monorepo this might be an individual package   
                     depending on your workflow                       
                                                                      
 --config            Path to the config file to use. Ivy will         
                     automatically search for .ivyconfig.json in the  
                     root directory if this is not passed explicitly  
                                                                      
 --config-json       You can pass the entire config contents as       
                     inline JSON. This is especially useful for LLM   
                     agents. This will override any .ivyconfig.json   
                     file                                             
                                                                      
 -h, --help          Print help                                       
                                                                      

By OnPurpose Studio
Ivy is created by OnPurpose Studio, a tech-first translation and
localization studio. We help dev teams code like a linguist.

Have a question? Hit us up 👉 https://onpurpose.studio/contact

```