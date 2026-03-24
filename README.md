# Ivy CLI for Translated Codebases

This is the repository for the npm package of Ivy, a CLI tool helps dev teams and LLM's observe and manage translations in their local codebase. It's written in Rust, and this repository contains the compiled binaries for Linux, Mac, and Windows.

Ivy is available to all clients of [OnPurpose Studio](https://onpurpose.studio). We'd love to get you a license. Please reach out!

## Install

```
npm i -g @onpurposestudio/ivy
```

## Setup

🚨 The below is for a Laravel codebase, but we can support any framework.

Create a `.ivyconfig.json` file in your project root with the following content:

```
{
  "token": "<your token>",
  "source_locale": "en_US",
  "resource_files": [
    {
      "file_type": "laravel_php",
      "patterns": [
        "./lang/<locale>/*.php"
      ]
    },
    {
      "file_type": "laravel_json",
      "patterns": [
        "./lang/<locale>.json"
      ]
    }
  ]
}
```

Note that `ivy` supports any number of resource file locations and types.

## Usage

In your project root you can now run ivy:

```
npx ivy --help
```

## Documentation

We've baked our entire documentation into `ivy --help` itself. This makes it very easy for LLM's to move as quickly as you do.

```
$ npx ivy --help
Ivy for Dev Teams
This is a CLI tool that dev teams and LLMs can use to simplify the process
of managing and translating content within their codebase.

Ivy is paid software available to clients of OnPurpose Studio. If you'd
like a token, please reach out:

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

## FAQ

### What does it do?

Ivy works with any library, framework, and codebase. It helps manage the annoying process of dealing with translatable keys within a codebase. Use it to audit, clean, or translate translatable keys.

### Who is this for?

Ivy is for companies that have 5-10 developers working on one or more localized codebases.

### Where's the code?

This software is closed source, but we're happy to make it available to any company that would like to review it.

## Who makes it?

[OnPurpose Studio](https://onpurpose.studio) is a tech-first localization studio. We help companies improve their localization tech stack, audit TMS vendors, and generally improve the I18N processes within their company and codebase.

Interested to connect? We'd love to chat! https://onpurpose.studio/contact