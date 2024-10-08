# Yelp Restaurant Finder Tool

[Atomic_agents Index](../../../README.md#atomic_agents-index) / [Atomic Agents](../../index.md#atomic-agents) / [Lib](../index.md#lib) / [Tools](./index.md#tools) / Yelp Restaurant Finder Tool

> Auto-generated documentation for [atomic_agents.lib.tools.yelp_restaurant_finder_tool](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py) module.

- [Yelp Restaurant Finder Tool](#yelp-restaurant-finder-tool)
  - [PriceRange](#pricerange)
  - [YelpCategory](#yelpcategory)
  - [YelpSearchResultSchema](#yelpsearchresultschema)
  - [YelpSearchTool](#yelpsearchtool)
    - [YelpSearchTool().run](#yelpsearchtool()run)
  - [YelpSearchToolConfig](#yelpsearchtoolconfig)
  - [YelpSearchToolInputSchema](#yelpsearchtoolinputschema)
  - [YelpSearchToolOutputSchema](#yelpsearchtooloutputschema)

## PriceRange

[Show source in yelp_restaurant_finder_tool.py:39](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L39)

#### Signature

```python
class PriceRange(Enum): ...
```



## YelpCategory

[Show source in yelp_restaurant_finder_tool.py:17](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L17)

#### Signature

```python
class YelpCategory(Enum): ...
```



## YelpSearchResultSchema

[Show source in yelp_restaurant_finder_tool.py:78](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L78)

#### Signature

```python
class YelpSearchResultSchema(BaseIOSchema): ...
```

#### See also

- [BaseIOSchema](../../agents/base_agent.md#baseioschema)



## YelpSearchTool

[Show source in yelp_restaurant_finder_tool.py:110](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L110)

Tool for performing searches using the Yelp API based on the provided queries.

#### Attributes

- `input_schema` *YelpSearchToolInputSchema* - The schema for the input data.
- `output_schema` *YelpSearchToolOutputSchema* - The schema for the output data.
- `api_key` *str* - The API key for the Yelp API.
- `max_results` *int* - The maximum number of search results to return.

#### Signature

```python
class YelpSearchTool(BaseTool):
    def __init__(self, config: YelpSearchToolConfig = YelpSearchToolConfig()): ...
```

#### See also

- [BaseTool](./base_tool.md#basetool)
- [YelpSearchToolConfig](#yelpsearchtoolconfig)

### YelpSearchTool().run

[Show source in yelp_restaurant_finder_tool.py:136](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L136)

Runs the YelpSearchTool with the given parameters.

#### Arguments

- `params` *YelpSearchToolInputSchema* - The input parameters for the tool, adhering to the input schema.
- `max_results` *Optional[int]* - The maximum number of search results to return.

#### Returns

- [YelpSearchToolOutputSchema](#yelpsearchtooloutputschema) - The output of the tool, adhering to the output schema.

#### Raises

- `ValueError` - If the API key is not provided.
- `Exception` - If the request to Yelp API fails.

#### Signature

```python
def run(self, params: YelpSearchToolInputSchema) -> YelpSearchToolOutputSchema: ...
```

#### See also

- [YelpSearchToolInputSchema](#yelpsearchtoolinputschema)
- [YelpSearchToolOutputSchema](#yelpsearchtooloutputschema)



## YelpSearchToolConfig

[Show source in yelp_restaurant_finder_tool.py:105](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L105)

#### Signature

```python
class YelpSearchToolConfig(BaseToolConfig): ...
```

#### See also

- [BaseToolConfig](./base_tool.md#basetoolconfig)



## YelpSearchToolInputSchema

[Show source in yelp_restaurant_finder_tool.py:46](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L46)

#### Signature

```python
class YelpSearchToolInputSchema(BaseIOSchema): ...
```

#### See also

- [BaseIOSchema](../../agents/base_agent.md#baseioschema)



## YelpSearchToolOutputSchema

[Show source in yelp_restaurant_finder_tool.py:88](../../../../../atomic_agents/lib/tools/yelp_restaurant_finder_tool.py#L88)

#### Signature

```python
class YelpSearchToolOutputSchema(BaseIOSchema): ...
```

#### See also

- [BaseIOSchema](../../agents/base_agent.md#baseioschema)